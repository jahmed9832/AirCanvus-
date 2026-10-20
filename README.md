# 🎨 AirDraw Ultra — Touchless AI Whiteboard

An advanced, browser-based touchless whiteboard powered by **MediaPipe Tasks Vision** and **HTML5 Canvas**. Draw smoothly in thin air using hand gestures in real-time, or sketch directly with finger/stylus on any device — fully optimized for both **Mobile** and **Desktop**.

🌐 **Live Demo:** [https://jahmed9832.github.io/AirCanvus-/](https://jahmed9832.github.io/AirCanvus-/)  
*(Also accessible at [AirDraw.html](https://jahmed9832.github.io/AirCanvus-/AirDraw.html))*

---

## ⚡ What's New in this Upgrade?

- 🚀 **Zero-Hang Mobile Experience**: Removed buggy orientation locks and full-screen blocking prompts. The app now natively supports both **Portrait** and **Landscape** modes on iOS and Android without freezing or crashing.
- ⚡ **Ultra-Fast Parallel Loading**: MediaPipe Vision WASM and the Hand Landmark neural model load simultaneously alongside camera initialization, with an animated step-by-step progress indicator.
- 📱 **Mobile-First Responsive UI**:
  - **Portrait Mode**: Sleek glassmorphic floating bottom dock with 1-tap color picker, tools, and actions.
  - **Landscape & Desktop**: Collapsible industrial side-panel with rich controls.
  - **Camera Switcher**: 1-tap toggle between **Front (Selfie)** and **Back** cameras on smartphones.
  - **PiP Video Thumbnail**: Real-time camera feed with hand skeleton overlay in the top-right corner (can be minimized).
- ✍️ **Buttery-Smooth Calligraphic Strokes**: Powered by a tuned **One-Euro Filter** and spline interpolation, eliminating hand tremor while maintaining zero input latency.
- 🖐️ **Dual Input Support**: Supports both **Air Gestures** (touchless) and **Touch / Stylus / Mouse** drawing.
- 🌓 **Dynamic Canvas Theme**: Switch seamlessly between a crisp white whiteboard and a futuristic dark neon canvas.
- 🔒 **100% Client-Side Privacy**: All camera vision processing occurs entirely within your browser — no video or images are ever uploaded or sent over the network.

---

## 🖐️ Hand Gestures Guide

| Gesture | Hand Pose | Action |
| :--- | :--- | :--- |
| **☝️ Draw** | Index finger extended alone | Draw strokes or position geometric shapes |
| **✌️ Select** | Index + Middle fingers up | Move pointer / hover over buttons (~0.6s) to click |
| **🖐️ Erase** | Open palm (all fingers extended) | Eraser circle follows hand to wipe strokes |
| **✊ Idle** | Folded fist / relaxed hand | Lift pen without drawing |

---

## ⌨️ Desktop Keyboard Shortcuts

- `P` : Pen
- `H` : Glow / Highlighter
- `L` : Straight Line
- `R` : Rectangle
- `C` : Circle
- `E` : Eraser
- `X` : Clear Board
- `Ctrl + Z` : Undo
- `Ctrl + Y` : Redo
- `Ctrl + S` : Save Image
- `+` / `-` : Adjust Brush Thickness
- `F` : Toggle Fullscreen

---

## 🚀 Running Locally

Because the camera and MediaPipe WebAssembly require a secure context (`HTTPS` or `localhost`), run a lightweight local server:

### Python:
```bash
python -m http.server 8000
```
Then visit: `http://localhost:8000/` or `http://localhost:8000/AirDraw.html`

### Node.js:
```bash
npx serve .
```

---

## 🛠️ Built With

- **Google MediaPipe Tasks Vision**: Real-time 21-point 3D hand landmark detection
- **HTML5 Canvas 2D**: Hardware-accelerated drawing engine with offscreen buffering
- **One-Euro Filter**: High-performance adaptive jitter reduction algorithm
- **Vanilla CSS3 & Glassmorphism**: Responsive design system without bloated dependencies
