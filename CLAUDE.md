# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static single-page portfolio website for Gionata Garavani (Full Stack Developer). No build system, no package manager, no framework — just vanilla HTML/CSS/JS.

## Development

**Serving locally:** Open `index.html` directly in a browser, or use any static file server:
```bash
python3 -m http.server 8080
# or
npx serve .
```

**Styles:** The source is `scss/style.scss` → compiled to `css/style.css`. Edit `scss/style.scss` and compile with any SCSS compiler. Vendor CSS in `css/` should not be modified.

**No build, lint, or test commands exist.**

## Architecture

Single `index.html` with anchor-linked sections (`#home-section`, `#about-section`, `#resume-section`, `#skills-section`, `#services-section`, `#projects-section`, `#contact-section`). All custom JS lives in `js/main.js`.

### Key integrations

- **EmailJS** — handles contact form submissions client-side (service ID: `service_wtjop2j`, template ID: `template_e3nid6s`, public key in `main.js`)
- **SweetAlert2** — toast notifications for form feedback
- **jQuery 3.2.1** — DOM manipulation and event handling throughout `main.js`

### JS library responsibilities

| Library | Purpose |
|---|---|
| `owl.carousel.min.js` | Hero image slider, testimonial carousel |
| `jquery.stellar.min.js` | Parallax scrolling effects |
| `jquery.waypoints.min.js` | Scroll-triggered animations |
| `jquery.magnific-popup.min.js` | Project image lightbox |
| `jquery.animateNumber.min.js` | Animated counters (stats section) |
| `scrollax.min.js` | Custom scroll effects |

All vendor JS files in `js/` (except `main.js`) should not be modified. Same for vendor CSS in `css/` (except `style.css`).

### Assets

- `images/` — all portfolio images and favicon (`ggicon.ico`)
- `fonts/flaticon/` — custom icon font
- `files/GionataGaravaniCV_EN.pdf` — downloadable CV
