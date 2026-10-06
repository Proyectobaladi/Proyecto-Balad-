# Proyecto Baladí v0.8.1 · Mobile / PWA

Versión móvil/PWA basada en Proyecto Baladí v0.7/v0.8, preparada para publicarse con GitHub Pages y añadirse a la pantalla de inicio de un iPhone desde Safari.

## Qué se ha corregido en v0.8.1
- Versión visible: **v0.8.1**.
- Workflow de GitHub Pages incluido en `.github/workflows/pages.yml`.
- Despliegue como sitio estático, sin Jekyll ni proceso de build innecesario.
- `actions/configure-pages@v5`, `actions/upload-pages-artifact@v4` y `actions/deploy-pages@v4`.
- Permisos `pages: write` e `id-token: write` y dependencia implícita en un único job de despliegue.
- Ejecución manual disponible desde Actions (`workflow_dispatch`).
- `.nojekyll` incluido.
- Manifest y Service Worker preparados con rutas relativas, compatibles con una URL de proyecto de GitHub Pages.
- Service Worker actualizado a caché `v0.8.1`.
- Se conserva el banco, imágenes, notas, estadísticas, auditoría, reportes de errores y funciones de v0.7/v0.8.

## Publicación en GitHub Pages

1. Crea o usa el repositorio `Proyecto-Balad-` (o el nombre que quieras).
2. Sube **el contenido de este ZIP**, no el ZIP dentro del repositorio. En la raíz deben quedar `index.html`, `app.js`, `data.js`, `styles.css`, `manifest.webmanifest`, `sw.js`, `assets/` y `.github/`.
3. Si el repositorio tiene workflows antiguos de Pages, elimina/desactiva los anteriores para evitar ejecuciones duplicadas.
4. En GitHub abre **Settings → Pages**.
5. En **Build and deployment → Source**, selecciona **GitHub Actions**.
6. Ve a **Actions → Deploy Proyecto Baladí to GitHub Pages**.
7. Si no se ha lanzado automáticamente tras subir los archivos, pulsa **Run workflow**.
8. Espera a que el workflow aparezca completamente en verde.
9. En la ejecución correcta, GitHub mostrará la URL de Pages en el entorno `github-pages`.

La URL habitual de un repositorio de proyecto será similar a:
`https://TU-USUARIO.github.io/NOMBRE-DEL-REPOSITORIO/`

## Instalar en iPhone

1. Abre **la URL de GitHub Pages en Safari** (no desde la app Archivos).
2. Espera a que cargue Proyecto Baladí.
3. Pulsa **Compartir** (cuadrado con flecha hacia arriba).
4. Pulsa **Añadir a pantalla de inicio**.
5. Comprueba que el nombre sea **Proyecto Baladí**.
6. Pulsa **Añadir**.
7. Abre Proyecto Baladí desde el nuevo icono de la pantalla de inicio.

Para las funciones PWA/offline, la aplicación debe abrirse desde HTTPS. Abrir `index.html` directamente como archivo local no equivale a una instalación PWA.

## Si GitHub vuelve a mostrar “Cancelled”

- Comprueba que **Pages → Source** está en **GitHub Actions**.
- Comprueba que solo existe un workflow de despliegue de Pages activo.
- Abre la ejecución en **Actions** y entra en el job para ver el paso exacto que falla.
- Puedes volver a ejecutar el workflow con **Re-run jobs** o con **Run workflow**.

## Comprobaciones locales realizadas
- `node --check app.js` correcto.
- `node --check data.js` correcto.
- Manifest JSON válido.
- Iconos iOS/PWA presentes.
- Workflow de Pages presente.
