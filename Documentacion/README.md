# ColorFly 🎨

Generador de paletas de colores aleatorias construido con HTML, CSS y JavaScript puro (vanilla).

🔗 **Demo en vivo:** https://joseferrer-webdevelopment.github.io/ProyectoM1_JoseFerrer/

---

## Descripción

ColorFly es una landing page interactiva inspirada en herramientas como Coolors.co, que permite generar paletas de colores aleatorias en formato HSL y HEX. El proyecto fue desarrollado como entregable del Proyecto Integrador del Módulo 1, con énfasis en fundamentos de DOM, HTML semántico, CSS sin estilos inline, y JavaScript orientado a eventos.

## Características principales

- Generación de paletas de colores aleatorias con un solo clic
- Selector de cantidad de colores (6, 8 o 9)
- Visualización del código HEX de cada color generado
- Copiar el código HEX al portapapeles con un solo clic
- Microfeedback visual al copiar ("¡Copiado!")
- Algoritmo de generación que evita colores visualmente similares en la misma paleta
- Diseño accesible: labels asociados, foco visible por teclado, contraste verificado
- Diseño responsive optimizado para dispositivos móviles, con layout adaptado para pantallas pequeñas.

## Tecnologías utilizadas

- HTML5 semántico
- CSS3 (Flexbox, Grid, variables CSS)
- JavaScript (DOM, eventos, manipulación dinámica de elementos)
- Git y GitHub para control de versiones
- GitHub Pages para despliegue

## Cómo usar la aplicación

1. Abre la aplicación en el navegador (link de la demo arriba)
2. Selecciona la cantidad de colores que deseas generar (6, 8 o 9) en el menú desplegable
3. Haz clic en el botón "Generar Paleta" para crear una nueva paleta aleatoria
4. Haz clic en el ícono de copiar sobre cualquier color para copiar su código HEX al portapapeles

## Cómo ejecutar el proyecto localmente

1. Clona el repositorio:
   ```
   git clone https://github.com/joseferrer-webdevelopment/ProyectoM1_JoseFerrer.git
   ```
2. Abre la carpeta del proyecto en VS Code
3. Usa la extensión Live Server para abrir `index.html`, o simplemente abre el archivo directamente en tu navegador

## Cómo desplegar el proyecto

Este proyecto está desplegado con GitHub Pages directamente desde la rama `main`, sirviendo el `index.html` ubicado en la raíz del repositorio. Para desplegar tu propia copia:

1. Ve a la configuración del repositorio en GitHub (Settings → Pages)
2. En "Source", selecciona la rama `main` y la carpeta raíz (`/`)
3. Guarda los cambios y espera unos minutos a que GitHub genere el link de la demo

## Decisiones técnicas

- Se optó por JavaScript vanilla sin frameworks, generando los swatches dinámicamente con `createElement` y `appendChild`, en vez de tenerlos fijos en el HTML, para soportar la cantidad variable de colores (6, 8 o 9)
- La conversión de HSL a HEX se resuelve con una función matemática estándar basada en la especificación de color CSS
- Se implementó un algoritmo de distancia mínima entre matices (hue) para evitar que dos colores generados en la misma paleta se vean visualmente idénticos
- El layout utiliza una cadena de Flexbox anidada (`main` → `#generador` → `.swatches`) para que la paleta ocupe el 100% del alto disponible sin generar scroll
- Se priorizó la accesibilidad con outline visible en `:focus` para navegación por teclado, y labels correctamente asociados a los controles de formulario
-Se implementó un breakpoint único en 480px para adaptar la interfaz a dispositivos móviles, redistribuyendo las proporciones de flexbox entre el título, la paleta y los controles para que el contenido completo sea visible sin necesidad de scroll
-Se resolvió un bug conocido de Safari en iOS relacionado con la unidad `100vh`, que no calcula correctamente el alto visible cuando la barra de direcciones del navegador cambia de tamaño dinámicamente; se solucionó utilizando la unidad moderna `100dvh` (dynamic viewport height)
-En mobile se priorizó la usabilidad táctil sobre la legibilidad completa del código HEX, mostrando el ícono de copiar de forma más grande y visible (sin depender del estado `:hover`, inexistente en pantallas táctiles), bajo la premisa de que el usuario prioriza copiar el color antes que leerlo letra por letra

## Mejoras futuras

- Bloqueo individual de colores para regenerar solo el resto de la paleta
- Guardado de paletas favoritas usando localStorage
- Animaciones adicionales en la transición entre paletas
- Alternar entre formato HEX y RGBA para mostrar el código de color
- Versión responsive optimizada para tablets

## Estructura del proyecto

```
ProyectoM1_JoseFerrer/
├── index.html
├── css/
│   └── style.css
├── scrip/
│   └── script.js
└── Documentación/
    ├── README.md
    ├── capturas/
    └── documentacion-ia/
```

## Documentación del uso de IA

Este proyecto se desarrolló con apoyo de Claude (Anthropic) como herramienta de aprendizaje guiado, utilizada para resolver dudas conceptuales, depurar errores y mejorar la lógica de generación de colores. La documentación completa de los prompts utilizados, con capturas de pantalla de cada interacción relevante, se encuentra en la carpeta `Documentación/documentacion-ia`.

## Autor

José Ferrer
GitHub: [@joseferrer-webdevelopment](https://github.com/joseferrer-webdevelopment)
