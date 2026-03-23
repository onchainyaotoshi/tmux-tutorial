# CLAUDE.md — tmux-tutorial

## What is tmux-tutorial?

Interactive visual tutorial for tmux in Indonesian (Bahasa Indonesia). Single-page static site built with React + Tailwind CSS, deployed to Cloudflare Pages.

See [README.md](README.md) for full project documentation.

## Tech Stack

- **Frontend:** React 19 + Vite 6
- **Styling:** Tailwind CSS v4 + shadcn/ui (subset: card, badge, button, table)
- **Fonts:** Inter (sans) + JetBrains Mono (mono) via Google Fonts
- **Deploy:** Cloudflare Pages via GitHub Actions (`wrangler pages deploy`)

## Project Structure

```
src/
  App.jsx              — Root component, renders AboutTmux with layout
  main.jsx             — Entry point
  index.css            — Tailwind directives + shadcn dark theme CSS vars
  lib/utils.js         — cn() helper (clsx + tailwind-merge)
  components/
    AboutTmux.jsx      — The tutorial (all 6 sections, ~667 lines)
  components/ui/       — shadcn/ui primitives
    card.jsx
    badge.jsx
    button.jsx
    table.jsx
index.html             — HTML shell with Google Fonts + dark mode
vite.config.js         — Vite + React + Tailwind v4, @ alias → src/
```

## Commands

```bash
npm run dev       # Vite dev server
npm run build     # Production build → dist/
npm run preview   # Preview production build locally
```

## Key Decisions

- **No router** — Single page, no client-side routing needed.
- **No backend** — Fully static site. No API calls.
- **`@` alias** — `@` maps to `src/` (vite.config.js + jsconfig.json). All shadcn imports use `@/lib/utils`.
- **Dark theme only** — `<html class="dark">` hardcoded. CSS vars in `src/index.css`.
- **Content language** — All tutorial text is in Indonesian (Bahasa Indonesia).

## Origin

Extracted from [tmux-api](https://github.com/onchainyaotoshi/tmux-api) `src/frontend/pages/AboutTmuxPage.jsx`. The only change from the original: function renamed from `AboutTmuxPage` to `AboutTmux`.
