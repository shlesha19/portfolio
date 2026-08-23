# SLASHH — Portfolio

Personal portfolio site for **Shlesha Gupta** (`slashh.ai`) — robotics, perception, autonomy and physical AI.

Built as a single self-contained `index.html`: no build step, no dependencies, no framework. Open the file and it runs.

## Structure

```
index.html      # markup, styles and scripts in one file
assets/         # photography
```

## Local preview

Open `index.html` directly in a browser, or serve it:

```bash
python -m http.server 8000
# http://localhost:8000
```

## Notes

- Project and lab data live in the `projects` / `experiments` arrays near the top of the `<script>` block — add entries there and the mission grid, filters and dossier modals pick them up automatically.
- Motion is gated behind `prefers-reduced-motion`, and a `<noscript>` fallback plus a load failsafe keep the page readable without JavaScript.
- Cards without a photo render a generated schematic derived from the project name, so the grid stays visually complete.

## Deploy

Any static host works. For GitHub Pages: **Settings → Pages → Deploy from branch → `main` / root**.
