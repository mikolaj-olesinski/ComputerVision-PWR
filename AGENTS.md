# AGENTS.md

Computer Vision course labs (PWr). All documentation, code comments, notebook text and plot labels are in **English**.

## Environment
- Package manager: **uv** (Python 3.12). Use `uv sync`, `uv run <cmd>`, `uv add <pkg>`. Never `pip install`.
- Do not commit `.env`, tokens, `.DS_Store`, local settings. Never print the GitHub token.
- Push to `main` only when the user asks.

## Layout
- `labN/` – one directory per lab (notebooks, images, theory). Notebooks reference images by relative path.

## OpenCV
- No magic numbers where OpenCV has a named constant. Use `cv2.COLOR_BGR2GRAY`, `cv2.THRESH_BINARY`, `cv2.BORDER_REFLECT`, `cv2.INTER_LINEAR`, etc., never their integer values.
- Other unavoidable numbers (thresholds, kernel sizes) go into named variables defined once, e.g. `THRESHOLD = 128`.

## Notebooks
- All imports in the first code cell, at the top.
- Data loading (images, files) goes in its own separate cell, apart from processing and plotting cells.
- Keep text minimal: short English markdown only where it is needed. No emojis, no long explanations.
- Keep cells small and focused; outputs must be reproducible (fixed seeds).

## Plots
- All titles, axis labels, legends and tick labels in English.
- Axes always visible and labelled (with units where applicable). Titles for every subplot.
- Clear, high-contrast colors. A given variable/series keeps the **same color across all plots** (define a color dict/constants once, e.g. `COLORS = {"R": "tab:red", ...}`).
- Images shown with `plt.imshow`: convert BGR to RGB first; use `cmap="gray"` for single-channel.
- Review every plot a second time after rendering: check that labels, axes, legends and colors are readable and nothing overlaps or is clipped. Fix before moving on.
