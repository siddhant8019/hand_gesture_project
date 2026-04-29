# Hand Gesture Project

A browser-based hand-gesture controlled visual experience. It uses
[MediaPipe Hand Landmarker](https://developers.google.com/mediapipe) to track
your hand from a webcam in real time and triggers a set of GPU-driven
particle/shader effects rendered with [Three.js](https://threejs.org/).

No installs, no build step — just a single HTML file and a webcam.

## Demo

![Hand Gesture Project demo](demo.gif)

## Features

The main experience (`index.html`) maps four hand poses to four distinct
particle/volume effects:

| Effect | Trigger gesture | Description |
|---|---|---|
| **Hollow Purple** | "Pinch" — thumb + index touching | A chaotic singularity combining attraction and repulsion |
| **Infinite Void** | "Cross" — index + middle fingers crossed | A multi-layered celestial domain with an event horizon ring and a vertical stream of information |
| **Cursed Reversal: Red** | Index finger pointing up | A blinding white-hot core generating a violent, jagged sphere of repulsive force |
| **Malevolent Shrine** | Flat hand / prayer gesture | A dark, ominous aura |

A separate **solar-system viewer** (`solar-system.html`) ships in this repo as
a JARVIS-style HUD over a procedural three.js solar system. It runs
independently of hand tracking.

## Getting Started

### Prerequisites

A modern browser (Chrome, Edge, Firefox, Safari) with webcam access.

### Run it

1. Clone the repo:
   ```bash
   git clone https://github.com/siddhant8019/hand_gesture_project.git
   cd hand_gesture_project
   ```

2. Open `index.html` in a browser. The easiest way during development is the
   "Live Server" VS Code extension — right-click `index.html` →
   *Open with Live Server*. You can also run any static file server, e.g.:
   ```bash
   python3 -m http.server 8000
   # then visit http://localhost:8000/index.html
   ```

3. Allow webcam access when prompted, hold a hand in view, and try the
   gestures listed above.

To try the solar system viewer instead, open `solar-system.html` the same way.

## Tech

- [MediaPipe Tasks Vision](https://developers.google.com/mediapipe) — hand landmark detection in the browser
- [Three.js](https://threejs.org/) — WebGL rendering, particle systems, and shaders
- Plain HTML/CSS/JS — no bundler, no framework

## License

This project is released under the [MIT License](LICENSE).
