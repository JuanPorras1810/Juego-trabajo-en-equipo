# Memoria del proyecto: Trabajo en equipo - Cuando el silencio esconde una crisis

## Descripcion

Este proyecto es un juego educativo basado en la situacion **El cuello de botella y la falta de empatia**.

Participan dos equipos que responden doce preguntas sobre planificacion, trabajo colaborativo y gestion de crisis: seis de seleccion multiple y seis de verdadero o falso. Cada equipo recibe seis preguntas, con exactamente tres de cada tipo. Cada equipo acumula puntos y conserva vidas. Al terminar, gana el equipo con mas vidas; si empatan, gana el equipo con mas puntos.

## Tecnologias

- HTML
- CSS
- JavaScript puro
- Google Fonts

No utiliza frameworks ni necesita instalar dependencias.

## Archivos principales

### `index.html`

Contiene la pantalla inicial, los campos para nombrar los equipos, el tablero de juego, las preguntas, el panel de justificacion, la pantalla de resultados y el modal de instrucciones.

### `style.css`

Contiene el diseno visual, los colores, el estilo retro arcade, el HUD de puntos y vidas, las animaciones y la adaptacion para pantallas pequenas.

### `script.js`

Contiene las preguntas, las respuestas correctas, las justificaciones, el cambio de turnos, el sistema de puntos y vidas, la seleccion del ganador y el reinicio de la partida.

## Funcionamiento actual

1. El usuario escribe el nombre del Equipo 1.
2. El usuario escribe el nombre del Equipo 2.
3. Se presiona **Comenzar mision**.
4. Se muestra el contexto completo del caso.
5. Una ruleta animada elige al equipo que inicia.
6. El juego mezcla las preguntas en pares equilibrados: cada par contiene una pregunta de seleccion multiple y una de verdadero o falso.
7. Los equipos alternan turnos, por lo que cada uno recibe tres preguntas de cada tipo.
8. Se indica si la respuesta fue correcta o incorrecta.
9. Se muestra la justificacion y se presiona el boton para continuar.
10. Se muestra el resultado final y el equipo ganador.

## Reglas

- Cada equipo comienza con 3 vidas.
- Una respuesta correcta suma 50 puntos base mas 5 puntos por cada segundo restante.
- Una respuesta incorrecta quita 1 vida.
- Las respuestas se bloquean despues de elegir una opcion.
- La respuesta correcta queda resaltada.
- Cada pregunta muestra su justificacion antes de pasar al siguiente turno.
- Si la respuesta es incorrecta, se muestra por que la opcion elegida esta mal y debajo se muestra la respuesta correcta con su justificacion.
- Si la respuesta es correcta, se muestra la respuesta correcta y su justificacion.
- Cada pregunta de seleccion multiple tiene un limite de 60 segundos.
- Cada pregunta de verdadero o falso tiene un limite de 30 segundos.
- Un acierto otorga una bonificacion por rapidez: 50 puntos base mas 5 puntos por cada segundo restante.
- Si se agota el tiempo, se pierde una vida y se muestra la explicacion de la respuesta correcta.
- Si un equipo pierde sus 3 vidas, la partida termina inmediatamente despues de mostrar la explicacion de la ultima respuesta.
- Si un equipo se queda sin vidas, pierde inmediatamente, aunque tenga mas puntaje.
- Si se terminan las preguntas y ambos equipos conservan vidas, gana el equipo con mayor puntaje.
- Si los equipos terminan con el mismo puntaje y ambos conservan vidas, se muestra un empate.
- La partida se guarda automaticamente en el navegador mediante `localStorage`.
- Si se recarga la pagina, se restauran los equipos, puntos, vidas, pregunta actual, turno, tiempo restante y explicacion pendiente.
- El boton de reinicio inicia una partida nueva y elimina la partida guardada anterior.
- El ganador se determina primero por cantidad de vidas.
- Si hay empate en vidas, se comparan los puntos.
- Si tambien empatan en puntos, se muestra un empate.

## Preguntas actuales

### Pregunta 1: Planificacion y metodo

**Respuesta correcta:** Dividir el trabajo de forma autonoma, sin entregas parciales ni reuniones de revision.

**Justificacion:** El problema fue el metodo autonomo sin controles. Las entregas parciales y revisiones obligatorias habrian revelado el bloqueo con tiempo para reaccionar.

### Pregunta 2: Trabajo en equipo y empatia

**Respuesta correcta:** Prioriza las tareas individuales sobre la entrega final comun.

**Justificacion:** Un equipo comparte el resultado final. Decir “yo ya cumpli” pone la tarea individual por encima del objetivo comun y rompe la responsabilidad compartida.

### Pregunta 3: Gestion de crisis y decision

**Respuesta correcta:** Recomponer la carga, reducir el prototipo a lo esencial y redistribuir tareas.

**Justificacion:** La respuesta mas efectiva es crear un minimo viable: reducir el alcance, redistribuir tareas y trabajar juntos para proteger la entrega.

## Estilo visual

El juego utiliza una estetica retro arcade:

- Fondo oscuro con tonos azul, morado y verde.
- Colores neón para los elementos importantes.
- Fuentes pixeladas `Press Start 2P` y `VT323`.
- Sombras duras tipo videojuego.
- Paneles tipo HUD para vidas y puntos.
- Vidas representadas con corazones.
- Puntos destacados en amarillo.
- Equipo 1 identificado con azul.
- Equipo 2 identificado con morado.
- Animaciones para aciertos, errores y transiciones.

## Colores principales

```css
--blue: #52c8ff;
--purple: #a988ff;
--green: #42e2ab;
--red: #ff7897;
```

## Como ejecutar el proyecto

No se necesita instalar nada. Abrir `index.html` en un navegador:

- Google Chrome
- Microsoft Edge
- Firefox

Se necesita internet para cargar las fuentes de Google Fonts. Sin internet, el juego sigue funcionando con fuentes alternativas.

## Como continuar en otro computador

Copiar la carpeta completa manteniendo estos archivos:

```text
Juego/
├── index.html
├── style.css
├── script.js
└── MEMORIA.md
```

Antes de modificar el proyecto, leer este archivo y revisar los tres archivos principales.

## Estado actual al cierre de la sesion

### Titulo actual

El nombre visible del briefing y el titulo de la pestaña son:

**Trabajo en equipo: Cuando el silencio esconde una crisis**

### Flujo completo

1. Se escriben los nombres del Equipo 1 y del Equipo 2.
2. Se presiona **Comenzar mision**.
3. Se muestra el contexto completo de la situacion.
4. La ruleta animada decide que equipo comienza.
5. Se presentan 12 preguntas en turnos alternos.
6. Cada respuesta muestra su resultado y justificacion.
7. Se presiona el boton para continuar al equipo contrario.
8. La partida termina si un equipo pierde sus 3 vidas o cuando se terminan las preguntas.
9. Si se terminan las preguntas y ambos equipos conservan vidas, gana el equipo con mas puntos.

### Distribucion de preguntas

Hay 12 preguntas equilibradas:

- 6 preguntas de seleccion multiple.
- 6 preguntas de verdadero o falso.
- Cada equipo recibe exactamente 3 preguntas de seleccion multiple y 3 de verdadero o falso.
- `balancedDeck()` crea pares de tipos distintos y luego los mezcla.

### Tiempo y puntos

- Seleccion multiple: 60 segundos.
- Verdadero o falso: 30 segundos.
- Acierto: 50 puntos base mas 5 puntos por cada segundo restante.
- Error: pierde 1 vida.
- Tiempo agotado: pierde 1 vida y solo se muestra la respuesta correcta con su explicacion.

### Reglas de victoria

- Si un equipo llega a 0 vidas, pierde inmediatamente aunque tenga mas puntos.
- Si ambos equipos conservan vidas al terminar las 12 preguntas, gana el de mayor puntaje.
- Si ambos conservan vidas y empatan en puntos, se muestra un empate.

### Guardado automatico

La partida se guarda en `localStorage` usando la clave:

```text
mision-entrega-final-partida
```

Se guardan los nombres, puntos, vidas, orden de preguntas, pregunta actual, turno, tiempo restante y una explicacion pendiente. Si se recarga la pagina, la partida se restaura.

- **Jugar otra vez** inicia una nueva partida conservando los nombres actuales del marcador.
- **Cambiar equipos** elimina la partida guardada y permite comenzar con otros nombres.
- Si se guardo un nombre incorrecto, usar **Cambiar equipos** antes de iniciar otra partida.

### Funcion de explicaciones

- Si se elige una respuesta incorrecta, aparece por que la opcion elegida esta mal y debajo la respuesta correcta con su justificacion.
- Si se elige la respuesta correcta, aparece la respuesta correcta y su justificacion.
- Si se acaba el tiempo sin elegir, no se muestra el bloque de respuesta incorrecta porque el equipo no eligio ninguna opcion.

### Verificacion realizada

El archivo `script.js` fue comprobado con:

```text
node --check script.js
```

La comprobacion fue correcta al cerrar la sesion.

## Posibles mejoras futuras

- Agregar mas preguntas.
- Incorporar sonidos retro y boton de silencio.
- Agregar musica de fondo.
- Agregar cronometro por pregunta.
- Crear niveles de dificultad.
- Permitir mas de dos equipos.
- Guardar resultados.
- Agregar tabla de posiciones.
- Agregar confeti y efectos de victoria.
- Permitir configurar la cantidad inicial de vidas.

## Reglas para futuros cambios

- Mantener la estetica retro arcade.
- No eliminar el sistema de vidas.
- No eliminar las justificaciones.
- Mantener los turnos alternos.
- Mantener la ruleta inicial y la distribucion equilibrada de preguntas.
- Mantener el contexto visible antes de comenzar las preguntas.
- Mantener los nombres personalizados de los equipos.
- Verificar la sintaxis de `script.js` despues de cambios.
- Probar el juego abriendo `index.html`.
- Actualizar este archivo cuando se agreguen funcionalidades importantes.

## Verificacion rapida

Desde la carpeta del proyecto se puede comprobar la sintaxis de JavaScript con:

```text
node --check script.js
```
