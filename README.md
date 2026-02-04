# Void Garden

**Void Garden** is an interactive, generative audio-visual art piece built with vanilla JavaScript. It functions as a "digital zen garden" where users create glowing, musical entities that drift through a void.

The project focuses on atmosphere, procedural generation, and real-time interaction using additive color blending and synthesized audio. It features a fully responsive control panel allowing users to manipulate the physics and aesthetics of the simulation in real-time.

### [Live Demo](https://siddhi17sharma.github.io/void-garden/)


## Key Features

* **Generative Audio Engine:** Uses the Web Audio API to generate sound in real-time without external assets. Pitch is calculated based on the screen's Y-axis using a Pentatonic scale.
* **Interactive Control Panel:** A GUI allows users to customize simulation parameters on the fly:
* **Shape Selection:** Toggle between Orbs, Stars, and Geometric Lotuses.
* **Physics Control:** Adjust particle speed, size, and lifespan.
* **Rainbow Mode:** Cycles through the full color spectrum for every new particle.


* **Procedural Visuals:** Every entity is unique, with randomized velocity, rotation, and pulse rates.
* **High-End Rendering:**
* **Additive Blending:** Uses `globalCompositeOperation = 'lighter'` to simulate realistic light blending.
* **Motion Trails:** Uses a semi-transparent clear loop to create vapor trails behind moving objects.


* **Zero Dependencies:** Built entirely in native HTML5 Canvas and JavaScript. No libraries or frameworks.

## Controls

### Mouse & Touch

* **Click/Tap:** Spawn a flower and trigger a musical note.
* **Hover Left Edge:** Reveal the Control Panel.

### Keyboard Shortcuts

* **1:** Select Orbs
* **2:** Select Stars
* **3:** Select Lotus
* **R:** Random Shape Mode
* **Space:** Toggle Rainbow Mode
* **C:** Clear Screen

## Technical Details

* **Language:** JavaScript (ES6+)
* **Rendering:** HTML5 Canvas API
* **Audio:** Web Audio API (`AudioContext`, `OscillatorNode`)
* **Hosting:** GitHub Pages

### Audio Logic

The application maps the user's vertical input position to a frequency array. High-screen clicks trigger high frequencies, while low-screen clicks trigger low frequencies.

```javascript
// Pitch mapping logic
const percentage = 1 - (y / height);
const index = Math.floor(percentage * scale.length);
const frequency = scale[Math.min(index, scale.length - 1)];

```

## Local Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/void-garden.git

```


2. Navigate to the directory:
```bash
cd void-garden

```


3. Open `index.html` in any modern web browser.

## License

This project is open source and available for personal and educational use.
