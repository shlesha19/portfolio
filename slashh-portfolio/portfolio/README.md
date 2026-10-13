# SLASHH.EXE — Portfolio

Personal portfolio site for **Shlesha Gupta** (`slashh.ai`) — robotics, perception, autonomy and physical AI.
Pixel-art / cyberpunk skin in void black, ultraviolet and electric blue.

Built as a single self-contained `index.html`: no build step, no dependencies, no framework. Open the file and it runs.

## Structure

```
index.html      # markup, styles and scripts in one file
assets/         # photography (pixelated at runtime — originals untouched)
```

## Local preview

```bash
python -m http.server 8000
# http://localhost:8000
```

## Notes

- The Photo Mode album reads from the `photos` array (src, caption, tile size) — add a file to `assets/` and a line there.
- Quest (project) and lab data live in the `projects` / `experiments` arrays at the top of the `<script>` block; the inventory lives in `techNodes`.
- Pixel icons are tiny text bitmaps in `SPRITES` — edit the strings to redraw them.
- The hero city is generated on a low-res canvas each load; photos are pixelated via canvas and "enhance" to full resolution on hover / tap.
- Player-card stat bars and ability XP bars are decorative — tune the `--v` values in the markup.
- Boot screen shows once per browser session. Motion is gated behind `prefers-reduced-motion`; a `<noscript>` fallback and a load failsafe keep the page readable.
- Easter egg: ↑ ↑ ↓ ↓ ← → ← → B A.

## Deploy

Any static host works (Vercel, Netlify, GitHub Pages). For GitHub Pages: **Settings → Pages → Deploy from branch → `main` / root**.
