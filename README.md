# Aprende Claude Code

Curso interactivo de Claude Code en 4 módulos. Cada lección es corta y tiene prácticas simuladas: una terminal, peticiones de permiso, reglas de permisos, hooks, `/rewind`, subagentes y reglas por área. Al final hay un reto y una referencia con buscador.

Son páginas estáticas, sin dependencias ni compilación.

## Qué hay en la web

Todas las páginas comparten la misma barra: Inicio · Instalación · Proyecto · Vuestro entorno · Construir vuestra app · Diapositivas · Reto final · Referencia.

- `index.html`: el curso interactivo (lecciones, reto final y referencia).
- `instalacion.html`: la guía de instalación. Es copia de `echevarne/guia-instalacion.html`: si cambias una, copia la otra.
- `proyecto.html`: la guía del proyecto Cadena de frío. La genera `guion-locucion/fuente/build_proyecto.py`. Cada paso al que enlaza una diapositiva lleva el enlace de vuelta a esa diapositiva («Diapositiva 20 ↗»): se calcula solo, leyendo las diapositivas.
- `entorno.html`: «Vuestro entorno», desde la sesión 4: las opciones para que Claude trabaje con el código de los asistentes (ficheros o IRIS) y las peticiones listas para pegar. Las diapositivas de la sesión 4 enlazan a sus pasos. Se escribe a mano.
- `construir.html`: «Construir vuestra app», desde la sesión 5: la novedad de cómo revisa código Anthropic (`REVIEW.md`) y las diez piezas del arnés para construir una app nueva (especificación, glosario, decisiones, `DESIGN.md`, integraciones simuladas, qué compartir, plan, ejemplos, progreso y revisor), con sus peticiones. Las diapositivas de la sesión 5 enlazan a sus bloques. Se escribe a mano.
- `diapositivas/`: la crea `publicar-web` (no está en esta carpeta). `index.html` lista todas las diapositivas de cada sesión, para abrir cualquiera con un clic (`sesion-1.html#20`); lo genera `herramientas/indice-diapositivas.mjs`. En las diapositivas, el botón «Índice» de la barra de abajo vuelve aquí.

Los enlaces de las diapositivas a la guía se abren siempre en la misma pestaña («guia») y los de la guía a las diapositivas en otra («diapositivas»): con dos pestañas vas y vuelves sin acumular ventanas. Solo carga las fuentes de Google Fonts y, si no están disponibles, usa fuentes del sistema.

## Publicarlo

- **GitHub Pages:** doble clic en `herramientas\publicar-web.cmd`. Copia esta carpeta y las diapositivas (`diapositivas/sesion-N.html`) al repositorio `aprende-claude-code` de la organización KIBOMCG, lo sube y activa Pages. Repítelo cada vez que cambies algo.
- **En local:** abre `index.html` en el navegador.

El progreso de cada persona se guarda en su propio navegador (`localStorage`).

## La app del profesor (`app/`)

En el móvil hace falta https para instalar la app, así que la de cada asistente no se instala ahí. La del profesor sí: `herramientas\publicar-app.cmd` copia lo que ve el navegador de su `cadena-de-frio` del Escritorio (sin `servidor.js`, `.env`, tests ni `.claude`) a `app/` y publica la web. Se lanza durante la sesión 4 (13:45), nunca antes: es la solución. En la web no hay avisos a Teams.

