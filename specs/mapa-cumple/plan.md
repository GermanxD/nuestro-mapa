# Plan técnico

## Estructura
- `index.html`: página única (HTML, CSS y JS en el mismo archivo).
- `fotos/`: JPEG de 1600 px convertidos desde los HEIC con `sips`.

## Decisiones
- Mapa: Leaflet 1.9.4 (cdnjs) con teselas de OpenStreetMap teñidas de azul con un filtro CSS (las de CARTO piden llave de API). Es la única dependencia; se justifica porque dibujar calles reales a mano no es viable.
- Tipografías de Google Fonts: Cormorant Garamond (títulos), Nunito Sans (texto), Caveat (pies de polaroid).
- Scroll: `IntersectionObserver` activa el momento visible; el mapa usa `flyTo` y una polilínea de progreso.
- Datos: constantes `PAREJA` y `MOMENTOS` al inicio del script (fecha, coordenadas, título, frase, fotos). Las coordenadas y fechas salen de los metadatos de las fotos.
- Confeti y visor de fotos: implementados a mano con canvas y un `dialog`, sin librerías.

## Momentos (fecha local, agrupados por día y lugar)
5 jul, 9 ago, 29 ago, 12 sep, 15 sep, 21 sep, 25 sep (inicio), 25 oct (café), 25 oct (Fundidora), 27 oct, 2 nov, 4 nov, 7 nov (lectura), 7 nov, 7 nov (Fundidora, video), 8 nov. Los videos van en `videos/` como MP4 H.264 con su póster.
