# Proyecto Baladí v0.8 · Mobile / PWA

Versión móvil basada en v0.7, preparada para instalarse en iPhone desde Safari mediante «Añadir a pantalla de inicio» y para funcionar como PWA cuando se sirve desde HTTPS.

## Novedades de v0.8
- Interfaz optimizada para pantallas de iPhone.
- Manifest PWA y registro de Service Worker para caché/offline.
- Iconos de aplicación incluidos.
- Metadatos específicos de iOS (`apple-mobile-web-app-*`).
- Aviso en pantalla con el procedimiento de instalación en iPhone.
- Se conserva el banco, las imágenes originales, las notas, estadísticas, auditoría, reportes de errores y funcionalidades de v0.7.

## Instalación en iPhone
1. Publicar/servir la carpeta por HTTPS.
2. Abrir la dirección en Safari.
3. Pulsar Compartir → Añadir a pantalla de inicio.
4. Abrir el icono de Proyecto Baladí desde la pantalla de inicio.

Abrir `index.html` directamente como `file://` permite probar la web, pero las funciones PWA/offline del Service Worker requieren un contexto seguro (HTTPS o localhost).
