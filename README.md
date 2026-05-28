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
- Markup/View --> HTML (static pages) 
- Styling --> CSS (single `styles.css`) 
- Dev server --> `http-server` (npm devDependency) 
- Assets --> PNG images (stored in `assets/`) 

---

## System architecture / workflow overview

This is a client-side static prototype. There is no backend or database. The app is composed of a set of interlinked HTML pages that rely on CSS for layout and small inline JavaScript for navigation and UI scaling.

Workflow overview:

1. Browser loads `index.html` (landing page).
2. User navigates through pages via internal links / buttons (e.g., `Page2.html`, `Page3.html`, `Page4.html`, `ResultPage.html`).
3. Inline scripts handle page-scaling, simple navigation, and button click handlers.

---

## Folder structure

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


Key files:

- `index.html` — Landing/ comparison grid.
- `Page2.html` — Hint/ onboarding card.
- `Page3.html` — Hero/ main interaction page.
- `Page4.html`, `page4_f.html`, `page4_t.html` — game/question pages and result variants(true/ false).
- `ResultPage.html` — end/ summary screen.
- `styles.css` — global styling and layout rules.
- `assets/` — all images and icons used by pages.

For quick reference, open the main page: [index.html](index.html).

---

## Environment / .env

This is a static client-side project and does not require environment variables by default.

If you require an example for future integrations, add a `.env` file at the project root.

Add real values in a local `.env` (do NOT commit secrets).

---

## How to run locally

Prerequisites:

- Node.js (for `npm`) is recommended if you want to use the included `http-server` dev script.

Install dependencies and run:

```bash
npm install
npm run dev
```

This will start a small static server and open the app (script configured to open `Menu.html` by default). You can also open `index.html` directly in a browser for manual testing.

Notes:

- The `dev` and `start` scripts use `http-server` (see `package.json`).
- If you prefer a different static server (e.g., `live-server` or VS Code Live Server), it's safe to use those instead.

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

- Add lightweight JavaScript state handling to track score and session data (localStorage).
- Centralize navigation and replace inline scripts with a single `app.js` for maintainability.
- Add exit button to each page that directly connects it to the menu page.
- Add unit/ integration tests (Playwright or Cypress for UI flows).
- Add automated CI checks (linting, link-checks) and a GitHub Actions workflow for previews.

---
