# 🎰 LOYA Casino

Casino 3D que corre directamente en el navegador, sin instalar nada ni servidor propio. Incluye tragaperras, ruleta, cartas contra el bot o entre dos personas, una máquina de garra con figuras de colección, una estantería 3D y un regalo diario.

> Versión de prueba. Todo el progreso (monedas, colección, ajustes) se guarda en el propio navegador de cada persona con `localStorage`.

## Juegos y secciones

| Sección | Qué hace |
|---|---|
| **Tragaperras** | Tres rodillos 3D, premio mayor con aura de oro, fuego o arcoíris |
| **Ruleta** | Rueda 3D con bola, elección de color y botones de suerte |
| **Cartas** | Arrastra la carta al centro; contra el bot (aleatorio, con apuesta libre) o 2 jugadores en el mismo dispositivo |
| **Peluches** | Máquina de garra: mueves la garra, agarras y te toca una figura de rareza aleatoria |
| **Estantería** | Estante 3D para exhibir, nombrar y acomodar la colección, con mejoras de espacio |
| **Regalo diario** | Calendario semanal: de 10 monedas el lunes a 70 el domingo, solo se reclama el propio día |

Rarezas de las figuras: Normal, Plata, Oro, Diamante, Ultra, Mega y Único, cada una con su probabilidad, valor y aura de color.

## Panel de administrador

En la pantalla de inicio, toca el sol dorado (o el nombre **LOYA**) e inicia sesión con:

- Usuario: `admin`
- Contraseña: `admin`

Desde el panel (⚙) se pueden cambiar probabilidades, pagos, apuestas, símbolos y colores de la tragaperras, casillas de la ruleta, cartas, rarezas y auras, costos de la estantería, premios diarios, efectos de victoria y el multiplicador global de ganancias. Todo se guarda en el navegador de quien lo cambia.

> ⚠️ Estas credenciales están dentro del código del juego, así que **no son seguras**. Sirven para pruebas, no para proteger nada.

## Cómo ejecutarlo

Abre `index.html` en el navegador. Para evitar problemas, es mejor servirlo con cualquier servidor estático:

```bash
python3 -m http.server 8000
# luego abre http://localhost:8000
```

Necesita conexión a internet para cargar [three.js](https://threejs.org/) (r128, desde cdnjs) y las fuentes de Google Fonts.

## Publicarlo con GitHub Pages

1. Crea un repositorio nuevo en GitHub (por ejemplo `loya-casino`).
2. Sube todo el contenido de esta carpeta a la raíz del repositorio.
3. Ve a **Settings → Pages**.
4. En **Build and deployment**, elige **Deploy from a branch**, rama `main` y carpeta `/ (root)`.
5. Guarda. En uno o dos minutos tendrás la dirección `https://TU-USUARIO.github.io/loya-casino/` para compartir.

Cada persona que abra el enlace juega con su propio guardado local, sin necesidad de cuenta ni permiso.

## Estructura

```
index.html      Estructura de las pantallas
css/styles.css  Estilos
js/app.js       Lógica del juego y escenas 3D
.nojekyll       Evita el procesado de Jekyll en GitHub Pages
```

## Datos guardados en el navegador

Claves de `localStorage` que usa el juego (todas empiezan por `loya_`): ajustes, monedas, colección y regalo diario. En **Admin → General** hay un botón para borrar todo el progreso.

## Licencia

Aún sin definir. Si vas a hacer público el repositorio, añade un archivo `LICENSE` con la licencia que prefieras.
