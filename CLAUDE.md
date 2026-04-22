# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Static personal website for Nassos Kranidiotis, hosted on GitHub Pages at `nassoskranidiotis.com`. No build step, no package manager — edit files directly and push to deploy.

## Structure

- `index.html` — single-page application with all sections (Home, Profile, Projects, Science & Art, Follow Me)
- `style.css` — custom styles layered on top of Bootstrap 5
- `script.js` — back-to-top button logic and AOS initialization
- `assets/` — images (`.webp`, `.png`) and video (`vb1.mp4`)
- `gi/index.html` — redirect page to an external Glycemic Index app
- `CNAME` — custom domain configuration for GitHub Pages

## Key dependencies (CDN, no install needed)

- Bootstrap 5.3.3 (CSS + JS bundle)
- Bootstrap Icons 1.10.5
- AOS (Animate On Scroll) 2.3.4

## Local development

Open `index.html` directly in a browser, or serve it with any static file server:

```bash
python3 -m http.server 8080
```

## Deployment

Push to the `main` branch — GitHub Pages deploys automatically. The custom domain is configured via `CNAME` and DNS A records pointing to GitHub's IPs (see `notes.txt`).

## Architecture notes

- The site is a single HTML file structured as anchor-linked sections (`#home`, `#profile`, `#projects`, `#scienceart`, `#followme`).
- The video background (`assets/vb1.mp4`) uses `position: fixed; z-index: -1` so all sections scroll over it.
- The `#scienceart` section uses a parallax-style fixed background image (`scienceart-bg.webp`) with a dark overlay via `::before` pseudo-element.
- AOS is initialized twice: inline in `index.html` and again in `script.js` — the `script.js` call is the effective one (runs last).
