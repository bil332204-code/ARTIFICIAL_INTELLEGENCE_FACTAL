 HEAD
# Fractal Cosmos — T-Shirt Artwork Generator

A single-page, browser-based generative art tool that renders an original, cyberpunk-styled fractal composition using genuine recursive fractal mathematics — not a pre-made texture. Every structure in the piece (the Mandelbrot core, the trees, the hexagon rings, the spiral-seeded triangles) is computed live on an HTML5 Canvas, so zooming into any region reveals further self-similar structure rather than noise. Output is a print-ready, portrait 2000×2500px PNG designed for the front of a T-shirt.

## Description

The composition places a real escape-time Mandelbrot set at the center, framed by a glowing ring, and surrounds it with recursive fractal trees, nested hexagon fractals, and logarithmic spiral arms seeded with recursive Sierpinski triangles — all rendered over a layered deep-space background of nebula glow, a starfield, and HUD-style orbital rings. A seeded pseudo-random generator drives every layer, so each "variation" is a fresh, reproducible instance of the same underlying algorithms rather than a random image.

## Fractal Types Implemented

- **Mandelbrot Set** — escape-time algorithm (`renderMandelbrot`) with smooth/continuous coloring (using the standard `log(log|z|)` normalized iteration count) instead of hard color bands, masked into a circular medallion with a soft alpha-fade edge and rendered through a custom 7-stop color palette (deep violet → magenta → orange → cyan → white).
- **Recursive Fractal Trees** — `drawBranch()` is a true recursive branching function: each call draws a segment, then spawns 2–3 child branches at randomized spread angles and shrinking length (~66–75% per level), with color and glow shifting by recursion depth. Eight of these trees are arranged in 8-fold rotational symmetry around the core.
- **Nested Hexagon Fractal** — `nestedHex()` recursively draws a hexagon, then calls itself again at 60% of the radius with a rotation offset, producing a self-similar shrinking ring pattern; repeated in clusters around the core.
- **Sierpinski Triangles** — `sierpinski()` is a classic recursive triangular subdivision (splitting each triangle into 3 corner sub-triangles at the edge midpoints), seeded at multiple points and scales via `drawSierpinskiNode()`.
- **Logarithmic Spiral Arms** — 3 spiral arms sweep outward from the core, with Sierpinski-triangle nodes placed along each arm at progressively shrinking scale as the spiral radius grows.

All randomization (nebula/star layout, tree branch angles, Mandelbrot zoom jitter) is driven by a single seeded PRNG (`mulberry32`), so a given seed always reproduces the same artwork.

## Tools, Languages & Libraries

- **Language:** JavaScript (vanilla, ES5/ES6)
- **Rendering:** HTML5 Canvas 2D API (including an offscreen canvas for the Mandelbrot layer)
- **Libraries/Frameworks:** None — no external dependencies, no build step
- **Structure:** Single self-contained `.html` file (markup, CSS, and script all inline)

## Setup & Run Instructions

1. Download/clone the file:
   ```bash
   git clone <https://github.com/bil332204-code/ARTIFICIAL_INTELLEGENCE_FACTAL.git>
   cd <AI>
   ```
2. Open `code.html` directly in any modern browser (Chrome, Edge, Firefox) — no server, install, or build step required.
3. The fractal renders automatically on load.
   - **Regenerate Variation** — picks a new random seed and re-renders the nebula/star layout, tree branching, and Mandelbrot zoom point.
   - **Download High-Res PNG** — exports the full 2000×2500 canvas as `fractal-cosmos-tshirt-design.png`.

## Screenshot

![Fractal Cosmos Output](./fractal-cosmos-tshirt-design.png)

## Student Information

- **Name:** Bilal
- **Registration Number:**  573512
- **Institution:** NUST SEECS (National University of Sciences and Technology, School of Electrical Engineering and Computer Science)
- **Course:** ARTIFICIAL INTELLIGENCE
=======

