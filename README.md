# InspAIred — Game App

A lightweight, static HTML/CSS game that compares human-written and AI-generated inspirational posts across cultures. Built as a responsive, screen-scaled interactive prototype intended for research/demo use.

---

## Project snapshot

- Live remote (repository remote): `https://github.com/KeyaPatel03/InspAIred-Game-App.git`
- Vercel deployed link: https://inspaired-game-app.vercel.app/
- Paper link: https://arxiv.org/pdf/2404.12933
- Code & Database link: https://github.com/MichiganNLP/cross_inspiration
- Frontend: static HTML + CSS (no framework). Minimal dev tooling via `http-server` for local hosting.

---

## Features

- Multi-page interactive prototype with screen-scaling for different viewports.
- Comparison grid showing human vs AI examples with contextual imagery and flags.
- Hint/explanation pages before staring the game.
- Simple questions (select AI vs Human) with feedback pages for correct/incorrect answers.
- Designed for Exhibition demo to showcase Research Paper work and for quick user studies.

---

## Tech stack

| Area | Technology |
|---|---|
| Markup/View | HTML (static pages) |
| Styling | CSS (single `styles.css`) |
| Dev server | `http-server` (npm devDependency) |
| Assets | PNG images (stored in `assets/`) |

---

## System architecture / workflow overview

This is a client-side static prototype. There is no backend or database. The app is composed of a set of interlinked HTML pages that rely on CSS for layout and small inline JavaScript for navigation and UI scaling.

Workflow overview:

1. Browser loads `index.html` (landing page).
2. User navigates through pages via internal links / buttons (e.g., `Page2.html`, `Page3.html`, `Page4.html`, `ResultPage.html`).
3. Inline scripts handle page-scaling, simple navigation, and button click handlers.

---

## Folder structure

```
./
├─ index.html
├─ Page2.html
├─ Page3.html
├─ Page4.html
├─ Page5.html
├─ ... (additional page variants: page4_f.html, page4_t.html, etc.)
├─ ResultPage.html
├─ styles.css
├─ package.json
└─ assets/  (images/icons used across pages)
```

---

## How to run locally

Open index.html directly in a browser (double-click or use file → open).

---

## Deployment (Vercel)

This repository is static and is well-suited to be deployed on Vercel as a static site.

Steps to deploy:

1. Push the repository to GitHub 
2. Sign in to Vercel and click **Import Project** → **Import Git Repository** → select this repo.
3. Configure project settings:
   - Framework: `Other` / Static Site
   - Build Command: (leave empty)
   - Output Directory: `/` (root)
4. Click **Deploy**. Vercel will serve the static files directly.

Optional: set a custom domain and add analytics or environment variables from the Vercel dashboard.

---

## Future improvements / roadmap

- Centralize navigation and replace inline scripts with a single `app.js` for maintainability.
- Add exit button to each page that directly connects it to the menu page.

---
