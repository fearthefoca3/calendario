# Calendario de Misiones

Calendario de adviento con niveles y misiones. Cada nivel desbloquea una casilla, y cada casilla solo se abre a partir de su día de diciembre.

## Archivos

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La web completa: diseño, lógica y configuración |
| `manifest.webmanifest` | Permite añadirla a la pantalla de inicio del iPhone como una app |
| `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` | Iconos de la app |

## Configuración

Todo lo que se puede cambiar está al principio del `<script>` de `index.html`, en el bloque `CONFIG`:

- `codigoViaje`: código que desbloquea el calendario (por defecto `Navidad2026`)
- `xpPorNivel`: experiencia por nivel (por defecto 100)
- `misiones`: lista de misiones con su XP y cuántas veces se pueden hacer
- `premios`: texto opcional al abrir cada casilla (por defecto "Abre el cajón N")

## Modo pruebas

Añade `#pruebas` al final del enlace, por ejemplo `https://usuario.github.io/adviento/#pruebas`. En este modo no cuentan las fechas y el progreso se guarda aparte. El botón "Empezar de cero" lo borra todo.

## Dónde se guarda el progreso

En el navegador del móvil (localStorage). No hace falta servidor ni cuenta. Para que iOS no borre los datos, conviene añadir la web a la pantalla de inicio. En la pestaña Misiones hay botones para descargar y restaurar una copia de seguridad.

## Cambiar la temática

La web usa siempre estas tres imágenes de la carpeta `tema/`:

| Archivo | Dónde se ve | Tamaño recomendado |
|---|---|---|
| `tema/fondo.png` | Fondo de toda la página | Vertical, 1170 x 2532 |
| `tema/fondo-crear.png` | Tarjeta de crear personaje | 1000 x 1200 |
| `tema/fondo-nivel.png` | Tarjeta del avatar y el nivel | Apaisada, 1200 x 360 |
| `tema/fondo-panel.png` | Recuadro grande que engloba todo el contenido | Vertical, 1100 x 2400 |

Para cambiar la temática, sustituye el archivo por otro con **el mismo nombre** y la web cambia sola. No hace falta tocar el código. Las imágenes se ajustan para cubrir todo el espacio, así que conviene que la parte importante quede en el centro.
