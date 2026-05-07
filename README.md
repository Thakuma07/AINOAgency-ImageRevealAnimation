
# AINO Agency Image Reveal Animation

A modern, high-performance web project showcasing a creative **ASCII Image Reveal Animation**, inspired by AINO Agency. The animation dynamically converts images into a grid of ASCII characters, scrambles them for a staggered effect, and finally reveals the original images underneath.

This project was built with Vanilla JavaScript and HTML5 Canvas, and has recently been modernized to use **Vite** as its fast development build tool.

<img width="1565" height="838" alt="Screenshot 2026-05-07 164305" src="https://github.com/user-attachments/assets/e8271cc9-9bf5-4c17-976f-cf8111b3d781" />

## ✨ Features

- **ASCII Art Conversion**: Dynamically processes images on a hidden canvas, evaluating the brightness of pixels to map them to an ASCII character scale.
- **Scrambled Reveal Effect**: Characters animate and randomly scramble, staggering their appearance to create a high-tech "decoding" visual experience.
- **Vite Integration**: Instant server start, lightning-fast HMR (Hot Module Replacement), and optimized production builds.
- **Responsive Layout**: Utilizing CSS Grid for a visually engaging, scattered image gallery aesthetic.

## 🛠️ Tech Stack

- **HTML5 & CSS3** - For document structure and complex grid styling.
- **Vanilla JavaScript (ES6)** - No heavy frameworks; pure JS manipulating the DOM and the `CanvasRenderingContext2D` API.
- **Vite** - Next-generation frontend tooling for serving and bundling.

## 📁 Project Structure

```text
.
├── index.html       # The main entry point and gallery markup
├── script.js        # Core logic for the ASCII effect and Canvas rendering
├── styles.css       # Layout, typography, and styling
├── package.json     # Vite dependencies and NPM scripts
├── .gitignore       # Git ignore rules for node_modules and build outputs
└── img1.jpg ...     # (Provide your own images referenced in index.html)
```

## 🚀 Setup & Installation

Ensure you have [Node.js](https://nodejs.org/) installed on your machine.

1. **Clone or Download the Repository**
2. **Navigate to the Project Directory**
   ```bash
   cd "AINO Agency"
   ```
3. **Install Dependencies**
   ```bash
   npm install
   ```

## 💻 Usage

### Development Server
To start the local development server with Hot Module Replacement (HMR):
```bash
npm run dev
```
Open the provided URL (usually `http://localhost:5173/`) in your browser to view the project.

### Production Build
To create an optimized, minified production build:
```bash
npm run build
```
This will generate a `dist/` directory containing your optimized static assets.

### Preview Production Build
To test the production build locally before deploying:
```bash
npm run preview
```

## 🧠 How the Animation Works

1. **Image Processing**: The script loops over every `.ascii-reveal` image. It draws the image onto an off-screen sampling canvas.
2. **Brightness Mapping**: It evaluates the RGB values of localized sections to calculate a brightness score (`0` to `1`).
3. **Character Assignment**: The brightness score is mapped against a constant `ASCII_CHARS` string. Darker areas get dense characters (`#`, `X`), and lighter areas get sparse characters (`.`, ` `).
4. **Scramble Animation**: The characters are randomly scrambled using a `setInterval` loop before gradually settling into their correct form. Once settled, the canvas is hidden, revealing the original high-resolution image.
