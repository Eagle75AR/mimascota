# 🐾 Mis Gatitos: Rocco, Tom y Bigote

Sitio web del **Trabajo Práctico de Ciencias Naturales** sobre el gato doméstico, realizado por **Brisa González, 4to D** (Mar del Plata, Buenos Aires).

> Versión digital del trabajo de carpeta. Pensado para leer en el celular y para publicar en **GitHub Pages**.

---

## ✨ Qué hay en el sitio

- **Carátula** digital del trabajo
- **Conclusión** escrita por Brisa, con tarjetas de datos científicos (230 huesos, salta 5× su altura, etc.)
- **Las historias de Rocco, Tom y Bigote** (el larguísimo, la historia de Bigote el día de lluvia, Tom purgándose, etc.)
- **Sección de ciencia**: plantígrados vs digitígrados, endoesqueleto comparado, cuadro de toda la familia
- **Tabla de cuidados** (responsive: cards en mobile, tabla en desktop)
- **Galería** con las imágenes complementarias
- **Bibliografía** y mensaje final

### Funcionalidades interactivas

- 📱 Mobile-first, 100% responsive
- 🌗 Modo claro/oscuro (toggle con gatito)
- 🔍 Lightbox al tocar cualquier imagen
- ✨ Animaciones al hacer scroll (fade + slide)
- 🐾 Estela de patitas al hacer click
- 🎉 Easter egg: tocá el emoji del hero y cambia de gato
- ⬆️ Botón flotante "volver arriba"
- 🎨 Tipografías redondeadas (Nunito) + manuscrita (Caveat) para la firma de Brisa
- ♿ Respeta `prefers-reduced-motion`

---

## 📁 Estructura de archivos

```
masco/
├── index.html              ← el sitio entero (HTML + CSS + JS embebidos)
├── README.md               ← este archivo
├── 1.webp                  ← carátula
├── 2.webp                  ← Bigote descansando
├── 3.webp                  ← Tom purgándose
├── 4.webp                  ← El amor y los cuidados
├── 5.webp                  ← Rocco larguísimo
├── 6.webp                  ← Higiene
├── 7.webp                  ← Bigote nos eligió (historia)
├── 8.webp                  ← Temperatura de Bigote
├── 9.webp                  ← Compartir territorio
├── 10.webp                 ← Familia interespecie
├── 11.webp                 ← Tabla de cuidados
├── 12.webp                 ← Lola la hámster
├── 13.webp                 ← Plantígrados vs digitígrados
├── 14.webp                 ← Endoesqueleto
├── 16.webp                 ← Cuadro comparativo
├── 17.webp                 ← Tom jugando
├── 18.webp                 ← Mi familia interespecie (resumen)
├── QR.png                  ← (no se usa en el sitio; va impreso en la carpeta)
└── WhatsApp Image...jpeg   ← (no se usa; referencia física de la carpeta)
```

> **Nota:** El `index.html` referencia todas las imágenes con extensión `.webp`. Convertí los originales a `.webp` antes de subir (yo no los convertí porque era el paso que vos ibas a hacer).

---

## 🛠️ Conversión de imágenes a `.webp`

El sitio espera imágenes `.webp` para que pese poco en el celular. Podés convertirlas con varias herramientas:

### Opción 1 — Script rápido con `cwebp` (recomendado)

Si tenés [`cwebp`](https://developers.google.com/speed/webp/download) instalado:

```bash
for f in 1.png 2.png 3.png 4.png 5.png 6.png 7.png 8.png 9.png 10.png 11.png 12.png 13.png 14.png 16.png 17.jpeg 18.png; do
  cwebp -q 80 "$f" -o "${f%.*}.webp"
done
```

### Opción 2 — Squoosh (sin instalar nada)

[Squoosh.app](https://squoosh.app) → arrastrá cada imagen → elegí WebP, calidad 80 → descargá y renombrá a `1.webp`, `2.webp`, etc.

### Opción 3 — ImageMagick

```bash
magick mogrify -format webp -quality 80 *.png *.jpeg
```

---

## 🚀 Probarlo localmente

1. Convertí las imágenes a `.webp` (paso anterior).
2. Hacé doble click en `index.html`. Se abre en el navegador.
3. ¡Listo! No necesita servidor ni instalación.

> Si querés servirlo con un mini servidor local (opcional):
> ```bash
> python -m http.server 8000
> ```
> Después abrí `http://localhost:8000` en el navegador.

---

## 📤 Publicarlo en GitHub Pages

1. **Creá un repositorio nuevo** en GitHub (puede ser público o privado, da igual — Pages funciona con los dos si está activado en la cuenta).
2. **Subí todos los archivos** del sitio (index.html + las 17 imágenes `.webp` + README.md) a la rama `main` (o `master`), en la **raíz del repositorio**.
3. **Activá GitHub Pages**:
   - Repo → **Settings** → **Pages**
   - En *Source* elegí **Deploy from a branch**
   - Branch: `main` · Folder: `/ (root)`
   - Guardá
4. Esperá 1-2 minutos. Tu sitio queda disponible en:
   ```
   https://<tu-usuario>.github.io/<nombre-del-repo>/
   ```

### Tip: dominio personalizado (opcional)

Si querés que se vea en `misgatitos.com` o similar:
- Comprá el dominio
- En **Settings → Pages → Custom domain** poné el dominio
- Configurá los DNS en tu registrador (un CNAME apuntando a `<tu-usuario>.github.io`)

---

## 👩‍🎓 Créditos

- **Autora del trabajo:** Brisa González, 4to D
- **Diseño y desarrollo web:** [tu nombre / familia]
- **Materia:** Ciencias Naturales
- **Año:** 2026

Hecho con 💕 · 🐾 Rocco · Tom · Bigote
