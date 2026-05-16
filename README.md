# Playable 3D Portfolio (Single-File WebGL)

This project is a **single-file, physics-driven 3D portfolio** experience built in `index.html`.

Users do not scroll the page. Instead, they drive a procedural rover through a cyberpunk world to explore portfolio content.

## Highlights

- **Single file only**: everything lives in `index.html`.
- **Procedural 3D only**: no external `.glb/.gltf/.obj` assets.
- **CanvasTexture text system**: all in-world text is rendered with Canvas API and mapped onto Three.js planes.
- **Physics-based vehicle**: built with `cannon-es` `RaycastVehicle`.
- **Interactive zones**:
  - Spawn (intro)
  - Experience
  - Projects
  - Skills grid
  - Contact terminal

## Tech Stack

- **Three.js** (CDN import map)
- **cannon-es** (CDN import map)
- **HTML + CSS + JavaScript** (all inline in `index.html`)

## Controls

- `W` / `ArrowUp`: accelerate
- `S` / `ArrowDown`: reverse
- `A` / `ArrowLeft`: steer left
- `D` / `ArrowRight`: steer right
- `Space`: brake
- Mouse click: activate interactive pads/links

## Running Locally

Because this is an ES module + import map setup, run it via a local static server (recommended):

### Option 1: Python

```bash
python3 -m http.server 8080
```

Then open:

- `http://localhost:8080`

### Option 2: Node (serve)

```bash
npx serve .
```

## File Structure

- `index.html` — full application (scene, physics, input, UI, content)
- `README.md` — project documentation

## Notes

- Link opening uses `window.open(url, '_blank')`, so browser popup settings can affect behavior.
- If CDN resources fail to load (offline or blocked network), the scene will not start.
