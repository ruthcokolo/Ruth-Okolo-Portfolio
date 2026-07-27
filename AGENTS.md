# AGENTS.md

## Cursor Cloud specific instructions

This repository is a static personal portfolio website — plain HTML, CSS, and JavaScript with no build system, package manager, or dependencies.

- Structure: `public/portfolio.html` (page), `src/portfolio.css` (styles), `src/index.js` (mobile menu toggle), `images/` (assets).
- No dependencies to install, and there is no lint or automated test setup.
- Run the site with a static server from the repo root (not from `public/`), because `public/portfolio.html` references assets via parent-relative paths (`../src/portfolio.css`, `../src/index.js`, `../images/...`). Serving from the root keeps those paths valid.
  - Example: `python3 -m http.server 8000`, then open `http://localhost:8000/public/portfolio.html`.
- The only JS behavior is the `#menu-icon` hamburger toggle, which only appears at viewport widths <= 1285px (see the media query in `src/portfolio.css`).
