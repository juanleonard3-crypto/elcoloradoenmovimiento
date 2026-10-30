# 🎮 El Colorado en Movimiento

Juego de **realidad mixta de cuerpo entero** que se juega con la cámara web: te recorta en vivo y te mete caminando dentro de un pueblo 3D inspirado en **El Colorado (Formosa, Argentina)**. En el camino pasás por 6 lugares históricos, aprendés un dato de cada uno y respondés una pregunta con la mano.

> Proyecto didáctico · DIA — Didáctica con IA · «Aprendé jugando»
> Trayecto Técnico Profesional · Auxiliar en Inteligencia Artificial · Práctica Profesionalizante
> ISFD y T «República Federal de Alemania» · El Colorado, Formosa · Prof. Ariel Cóceres

## ▶️ Cómo se juega

| Movimiento | Qué hace |
|---|---|
| 🚶 Caminar en el lugar | Avanzar por el pueblo |
| ↔️ Un paso al costado | Cambiar de carril (hay 3) |
| ✋ Mano arriba | Agarrar frutas y estrellas, y pasar de la ficha a la pregunta |
| ✋ Mano izquierda / derecha / las dos | Responder **A** / **B** / **C** (hay que sostenerla unos segundos) |

1. Al empezar, ingresá tu peso (sirve solo para estimar calorías) y tocá **«¡Dale, empezamos!»**.
2. Parate a unos **2 metros** de la cámara, con la cabeza y las rodillas a la vista.
3. **Calibración de 3 segundos:** quedate quieto y de frente.
4. Recorré los 6 lugares: Hospital Provincial, Plaza General San Martín, Municipalidad (Comisión de Fomento), Comisaría (Subcomisaría «Bermejo»), E.P.E.P. N.º 166 «Dr. Luis María Drago» y Parroquia San Antonio de Padua.

**Puntajes:** ⭐ estrella +10 · 🥭 mango +25 · 🍉 sandía +50 · respuesta correcta +100 · 🐄 chocar con una vaca o una tronquera −20.

**Pantalla final:** puntaje, respuestas correctas, pasos en el lugar, tiempo en movimiento, obstáculos esquivados y calorías **estimadas** (≈ 3,5 × peso en kg × horas de juego en movimiento; es una estimación, no una medición).

**Sin cámara:** botón «Jugar con el teclado» → `↑` camina, `←`/`→` cambian de carril, `Espacio` hace de mano arriba, `A`/`B`/`C` (o `1`/`2`/`3`) responden, `F` pantalla completa.

## 🔒 Privacidad

Todo el procesamiento de la cámara ocurre **en tu propio dispositivo** con MediaPipe. Las imágenes **no se guardan ni se envían** a ningún servidor, y el video crudo ni siquiera se muestra en pantalla. Lo único que se descarga de internet son las librerías y el modelo de MediaPipe desde un CDN.

## 🚀 Publicarlo en GitHub Pages

1. Creá un repositorio nuevo en GitHub (por ejemplo `el-colorado-en-movimiento`).
2. Subí `index.html`, `README.md` y `.nojekyll` a la raíz.
3. En el repositorio: **Settings → Pages → Build and deployment → Deploy from a branch → `main` / `(root)` → Save**.
4. Esperá uno o dos minutos y entrá a `https://TU-USUARIO.github.io/el-colorado-en-movimiento/`.

GitHub Pages da **HTTPS**, que es lo que necesita Chrome para dejar usar la cámara (también en el celular).

### Probarlo en tu compu antes de subirlo
```bash
python -m http.server 8000
# abrí http://localhost:8000
```
Abrir `index.html` con doble clic puede andar, pero Chrome a veces bloquea la cámara en archivos locales.

## 📱 Celular
Funciona en Chrome con HTTPS. Apoyá el celular **fijo y en horizontal**, a unos 2 metros, con la cámara frontal. Es una versión inicial: el rendimiento depende del equipo.

## 🛠️ Detalles técnicos
- Un solo archivo `index.html` (HTML + CSS + JavaScript), sin instalación ni compilación.
- [Three.js](https://threejs.org/) r160 (MIT) y [MediaPipe Pose](https://developers.google.com/mediapipe) 0.5.1675469404 (Apache-2.0), cargados desde **jsDelivr** con versión fija.
- Modelo de pose liviano (`modelComplexity: 0`) con segmentación de persona para el recorte.
- Para una versión 100 % sin conexión hay que incrustar las librerías y los modelos dentro del archivo.

## 🧩 Si algo falla
| Problema | Probá |
|---|---|
| No pide la cámara | Usá HTTPS o `localhost`; revisá el permiso del sitio en Chrome |
| «No te veo» | Más luz, fondo menos cargado, alejate hasta que se vean cabeza y rodillas |
| No cuenta los pasos | Levantá bien las rodillas, alternadas, con las rodillas a la vista |
| Va lento | Cerrá otras pestañas y activá la aceleración por hardware de Chrome |
| Mensaje de error rojo al inicio | Anotalo y reportalo en *Issues* |

## 📚 Contenidos
Las fichas históricas (año de origen, dato histórico, curiosidad y fuente) vienen de archivos y testimonios locales de El Colorado. Si encontrás un dato para corregir, abrí un *Issue*.

## 📄 Licencia
A definir por el autor (agregá un archivo `LICENSE` antes de compartirlo).
