# AirDraw — Draw in the Air with Your Hand

> A browser-based air drawing app that uses your webcam and hand gestures to paint on a live camera feed. No installation, no plugins, no tracking.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Visit-00e0ff?style=for-the-badge)](https://minajuddin0510.github.io/Air-Drawing)
[![License](https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge)](LICENSE)
[![HTML](https://img.shields.io/badge/Built%20With-HTML%2FCSS%2FJS-f59e0b?style=for-the-badge)](#)

---

## ✋ How It Works

AirDraw uses **MediaPipe Hands** to detect your hand in real time through your webcam. Different finger gestures switch between draw, hover, and erase modes — no touch or mouse required.

---

## 🖐️ Gesture Controls

| Gesture | Action |
|---|---|
| ☝️ Index finger only | **Draw** — traces a stroke as you move |
| ✌️ Index + Middle finger | **Hover** — moves the cursor without drawing |
| 🖐️ Open palm (all fingers up) | **Erase** — wipes a circular area under your fingertip |

---

## ✨ Features

- **Live camera feed** as the drawing background
- **Mirror mode** — flips the camera so movement feels natural (toggle with `M`)
- **Exponential smoothing** — reduces jitter for cleaner strokes
- **Custom brush color** — full color picker
- **Adjustable brush size** — slider control
- **Adjustable eraser size** — slider control
- **Save drawing** — exports the camera frame + strokes as a merged PNG
- **Keyboard shortcuts** — `M` mirror · `C` clear · `S` save
- **Zero dependencies** — single HTML file, MediaPipe loaded from CDN
- **Responsive** — works on desktop and laptop webcams

---

## 🚀 Getting Started

> **Important:** This app requires camera access and must be served over `localhost` or `https`. Opening `index.html` directly as a `file://` URL will block camera permissions in most browsers.

### Option 1 — VS Code Live Server (recommended)

1. Clone the repo:
   ```bash
   git clone https://github.com/minajuddin0510/Air-Drawing.git
   cd Air-Drawing
   ```
2. Open the folder in VS Code
3. Install the **Live Server** extension
4. Right-click `index.html` → **Open with Live Server**
5. Allow camera permission when prompted

### Option 2 — Python local server

```bash
git clone https://github.com/minajuddin0510/Air-Drawing.git
cd Air-Drawing
python -m http.server 8080
# Open http://localhost:8080 in your browser
```

### Option 3 — GitHub Pages

```
https://minajuddin0510.github.io/Air-Drawing
```

---

## 🗂️ Project Structure

```
Air-Drawing/
└── index.html    # Entire app — self-contained single file
```

---

## ⌨️ Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `M` | Toggle mirror mode |
| `C` | Clear the canvas |
| `S` | Save merged image (camera + drawing) |

---

## 🛠️ Tech Stack

- **HTML5 Canvas** — overlay and drawing layers
- **MediaPipe Hands** — real-time hand landmark detection (via CDN)
- **MediaPipe Camera Utils** — webcam frame loop
- **Vanilla JavaScript** — zero frameworks, zero build step
- **CSS** — dark UI with glassmorphism accents

---

## 🌐 Browser Support

Works best in **Google Chrome** or **Microsoft Edge**. Firefox may have limited MediaPipe performance. Requires a working webcam and camera permission granted.

---

## 🤝 Contributing

Pull requests are welcome! Ideas for improvement:

- Multi-hand support
- Undo / redo stack
- Shape drawing mode (circles, lines, rectangles)
- Color palette gesture switching

```bash
git checkout -b feature/your-feature-name
```

---

## 📝 License

This project is licensed under the [MIT License](LICENSE).

---

## 👤 Author

**Minaj Uddin**
- GitHub: [@minajuddin0510](https://github.com/minajuddin0510)

---

> If you had fun drawing in the air, give it a ⭐ on GitHub!
