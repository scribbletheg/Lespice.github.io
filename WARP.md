# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

Repository: resume-website-template

Overview
- This is a static, single-page résumé/portfolio site using plain HTML, CSS, and a small amount of JavaScript. There is no build step, package manager, or test framework configured.
- Key files: index.html (content and structure), styles.css (theme, layout, print rules), script.js (UX: smooth scrolling, dynamic year).

Common commands
- Local preview
  - PowerShell (Python): python -m http.server 8000
    - Then open http://localhost:8000
  - Node.js: npx serve .

- Build: N/A (no build tooling configured)
- Lint: N/A (no linter configured)
- Tests: N/A (no test framework configured)

How to work in this codebase
- Edit content in index.html (name, contact, sections). The primary navigation uses in-page anchors that map to section IDs (e.g., #summary, #experience, #projects, #skills, #education, #contact).
- Adjust theming and spacing in styles.css. The file defines CSS custom properties for colors and includes responsive and print styles. Dark theme is the default; print styles hide header/nav/footer and simplify layout for PDF printing.
- script.js enhances UX:
  - Sets the current year in the footer (#year)
  - Smoothly scrolls to section anchors and moves focus for accessibility

Deploy (from README highlights)
- Initialize Git, set remote, and push main:
  - git remote add origin https://github.com/<your-handle>/resume-website-template.git
  - git push -u origin main
- Enable GitHub Pages for the main branch (root) in repository settings.

Notes
- For quick edits, you can also open index.html directly in a browser; using a local HTTP server is recommended for a closer-to-production context.
- If you later adopt tooling (e.g., a linter, bundler, or test runner), update this file with the new commands and any architectural changes.
