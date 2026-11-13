# Nuestro mapa — landing de cumpleaños

## Objetivo
Página de regalo por su cumpleaños 25 (13 de noviembre de 2026): un recorrido por los momentos que han vivido juntos, ubicados en un mapa a partir del GPS de las fotos.

## Alcance
- Incluye: portada, recorrido con mapa y fotos, contador de días, mensaje final con confeti.
- Fuente de fotos: solo `Desktop/fotos/fotos2` (41 HEIC, todas con GPS). Los videos `.mov` quedan fuera.
- Fuera de alcance: publicación en internet, música, edición de textos desde la página.

## Flujo
1. Portada: "Feliz cumpleaños", su nombre, el 25 y tres fotos tipo polaroid.
2. Recorrido: al hacer scroll, cada momento se activa, el mapa vuela a su pin y la ruta avanza hasta él.
3. El 25 de septiembre (inicio del noviazgo) se destaca con un pin y tarjeta especiales.
4. Contador: días de novios y días desde la primera foto, calculados al abrir.
5. Cierre: mensaje y confeti azul y blanco.

## Estados y casos borde
- Sin conexión o si el mapa no carga: las fotos y textos se leen igual; el mapa muestra un aviso discreto.
- Celular: mapa fijo arriba y momentos debajo; el mapa no atrapa el scroll.
- `prefers-reduced-motion`: sin vuelos animados ni confeti.
- Momentos en el mismo lugar: el pin activo queda encima.

## Criterios de aceptación
- Los 15 momentos aparecen en orden cronológico con fecha local de Monterrey y pin en su coordenada real.
- Al llegar a cada momento con scroll, el mapa se centra en su pin; tocar un pin lleva a su tarjeta.
- Paleta blanca y azul; se ve bien a 375 px y en escritorio, sin scroll horizontal.
- Nombre, títulos y frases se cambian en un solo bloque de datos al inicio del script.
