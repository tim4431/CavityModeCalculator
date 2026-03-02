# Interactive Cavity Mode Viewer

## Browser App

It can be accessed here:

[https://avkgithub1.github.io/CavityModeViewer](https://avkgithub1.github.io/CavityModeViewer)

The repository includes a static browser version of the cavity viewer:

- `index.html`
- `styles.css`
- `cavity-core.js`
- `app.js`
- `.nojekyll`

### Browser Features

The browser app view:

1. `index.html`
   Main cavity viewer for:
   - cavity geometry
   - wavelength and refractive index
   - cavity mode profile
   - `g1-g2` stability diagram

### Use Locally

Open `index.html` in a browser for a quick check, or serve the folder locally:

```powershell
python -m http.server 8000
```

Then visit `http://localhost:8000/`.

Recommended flow:

1. Open `index.html`
2. Set `R1`, `R2`, `L`, wavelength, and `n_center`
3. Inspect the cavity mode and stability plots

### Publish to GitHub Pages

This repo now includes a GitHub Actions workflow at `.github/workflows/deploy-pages.yml`.

1. Push the repository to GitHub.
2. In GitHub, open `Settings` > `Pages`.
3. Set `Source` to `GitHub Actions`.
4. Push to `main`, or run the workflow manually from the `Actions` tab.

The workflow uploads the repository root as a static site and deploys it to GitHub Pages automatically.
The `.nojekyll` file is kept so GitHub Pages serves the static files directly without trying to run Jekyll.

For a project repository, the site URL is typically:

```text
https://<your-github-username>.github.io/<repository-name>/
```

## Python Version

Python scripts are also included:

- `cavity-mode-display.py`
- `cavity-gui.py`

### Requirements

- numpy
- matplotlib
- PyQt6
