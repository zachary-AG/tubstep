# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

TubStep™ senior design portfolio website for Columbia University MECE E3430, Spring 2026, Team 11.

## Development

No build step. Open `index.html` directly in a browser, or serve locally:

```bash
python -m http.server 8080
# then visit http://localhost:8080
```

## Structure

- `index.html` — single file containing all HTML, CSS (`<style>`), and JS (`<script>`)
- `assets/` — images and videos dropped in by the team (placeholders in HTML until then)

## Architecture Constraints

- Plain HTML + CSS + vanilla JS only — no frameworks, no npm, no build tooling
- All styles live in a `<style>` block in `index.html`; all scripts in a `<script>` block at the bottom
- Asset placeholders are `<div class="img-placeholder">` styled as gray boxes — do not use external placeholder image services
- Section IDs must match nav anchor links: `#overview`, `#prototype`, `#prior-art`, `#exploded`, `#analysis`, `#team`
- Scroll animations use `IntersectionObserver` adding `.visible` class (opacity + translateY transition)
- Mobile breakpoint: 768px — all two-column layouts stack to single column
