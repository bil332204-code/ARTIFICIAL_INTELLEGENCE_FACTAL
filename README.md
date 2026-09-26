# Fractal Cosmos

**Interactive Generative Fractal Art in Vanilla JavaScript**

Fractal Cosmos is a browser-based generative art project that combines multiple mathematical fractals into a single interactive composition. The artwork is rendered live with the HTML5 Canvas API and can be regenerated with a new seed or exported as a high-resolution PNG.

This project was created for an Artificial Intelligence course activity at NUST SEECS and focuses on recursive design, procedural generation, and mathematical visualization.

## Highlights

- Real **Mandelbrot set** rendering using the escape-time algorithm with smooth coloring
- Recursive **fractal trees** with depth-based branching and variation
- Recursive **Sierpinski triangles**
- Nested **hexagon fractals**
- **Logarithmic spiral** layouts seeded with recursive geometry
- Seeded pseudo-random generation for reproducible variations
- Interactive **Regenerate Variation** control
- High-resolution **2000 × 2500 PNG export**
- No external libraries or build tools

## How It Works

The composition is generated entirely in JavaScript on an HTML5 canvas.

### Mandelbrot Core

The central artwork uses an escape-time Mandelbrot renderer. Each pixel is iterated in the complex plane until it either escapes or reaches the iteration limit. Smooth coloring is applied using a normalized iteration value instead of hard color bands.

### Recursive Fractal Trees

Each branch recursively generates smaller child branches with controlled angle and length variation. Multiple trees are arranged radially around the Mandelbrot core.

### Sierpinski Triangles

Triangles are recursively subdivided into three corner triangles using edge midpoints, producing classic self-similar Sierpinski geometry.

### Nested Hexagons

Hexagons recursively shrink and rotate, creating layered geometric structures around the central artwork.

### Spiral Composition

Three logarithmic spiral arms organize smaller recursive fractal elements around the center and help connect the different visual structures into one composition.

## Tech Stack

- **JavaScript**
- **HTML5 Canvas 2D API**
- **HTML / CSS**
- No frameworks
- No external dependencies

## Run Locally

Clone the repository:

```bash
git clone https://github.com/bil332204-code/ARTIFICIAL_INTELLEGENCE_FACTAL.git
cd ARTIFICIAL_INTELLEGENCE_FACTAL
```

Then open:

```text
index.html
```

in any modern browser.

No installation, package manager, or local server is required.

## Controls

**Regenerate Variation** generates another composition using a different random seed.

**Download High-Res PNG** exports the current artwork as a 2000 × 2500 PNG suitable for presentation or design use.

## Project Structure

```text
.
├── index.html
├── README.md
└── .gitignore
```

The full application is intentionally self-contained in `index.html`.

## Concepts Demonstrated

- Recursion
- Fractal mathematics
- Procedural generation
- Complex-number iteration
- Seeded pseudo-random generation
- Canvas-based rendering
- Interactive browser programming
- High-resolution image export

## Possible Improvements

- Add user-controlled Mandelbrot zoom and pan
- Allow direct seed input for reproducible artwork
- Add controls for recursion depth and color palette
- Split rendering logic into reusable JavaScript modules
- Publish the project with GitHub Pages

---

**Project:** Fractal Cosmos  
**Institution:** NUST SEECS  
**Course Context:** Artificial Intelligence
