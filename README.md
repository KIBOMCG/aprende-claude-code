# Aprende Claude Code

Curso interactivo de Claude Code en 4 módulos. Cada lección es corta y tiene prácticas simuladas: una terminal, peticiones de permiso, reglas de permisos, hooks, `/rewind`, subagentes y reglas por área. Al final hay un reto y una referencia con buscador.

Son páginas estáticas, sin dependencias ni compilación.

## Qué hay en la web

Todas las páginas comparten la misma barra: Inicio · Instalación · Proyecto · Diapositivas · Reto final · Referencia.

- `index.html`: el curso interactivo (lecciones, reto final y referencia).
- `instalacion.html`: la guía de instalación. Es copia de `echevarne/guia-instalacion.html`: si cambias una, copia la otra.
- `proyecto.html`: la guía del proyecto Cadena de frío. La genera `guion-locucion/fuente/build_proyecto.py`. Cada paso al que enlaza una diapositiva lleva el enlace de vuelta a esa diapositiva («Diapositiva 20 ↗»): se calcula solo, leyendo las diapositivas.
- `diapositivas/`: la crea `publicar-web` (no está en esta carpeta). `index.html` lista todas las diapositivas de cada sesión, para abrir cualquiera con un clic (`sesion-1.html#20`); lo genera `herramientas/indice-diapositivas.mjs`. En las diapositivas, el botón «Índice» de la barra de abajo vuelve aquí.

Los enlaces de las diapositivas a la guía se abren siempre en la misma pestaña («guia») y los de la guía a las diapositivas en otra («diapositivas»): con dos pestañas vas y vuelves sin acumular ventanas. Solo carga las fuentes de Google Fonts y, si no están disponibles, usa fuentes del sistema.

## Publicarlo

- **GitHub Pages:** doble clic en `herramientas\publicar-web.cmd`. Copia esta carpeta y las diapositivas (`diapositivas/sesion-N.html`) al repositorio `aprende-claude-code` de la organización KIBOMCG, lo sube y activa Pages. Repítelo cada vez que cambies algo.
- **En local:** abre `index.html` en el navegador.

El progreso de cada persona se guarda en su propio navegador (`localStorage`).

## Puntos de partida (`rescate/`)

La guía del proyecto (`proyecto.html`, «Si te quedas atrás») da a cada asistente un comando que descarga el proyecto tal como quedó al final de una sesión. Sale de `rescate/cadena-de-frio-sN.json`. Así no hay que mandar zips por correo ni adjuntos por Teams, que la empresa puede bloquear.

- Esos ficheros los genera `herramientas\preparar-sesion-N` a partir de la versión de referencia: el de la sesión anterior, nunca el de la que se va a dar.
- Los sube `herramientas\publicar-web` junto con el resto de la web, antes de la sesión (mejor el día antes). En la guía, esa parte tiene que decir «Disponible».
- Son las soluciones de las sesiones ya hechas: no subas ninguno antes de tiempo.
