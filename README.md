# tmux-tutorial

[![Deploy](https://github.com/onchainyaotoshi/tmux-tutorial/actions/workflows/deploy.yml/badge.svg)](https://github.com/onchainyaotoshi/tmux-tutorial/actions/workflows/deploy.yml)
[![Built with Cloudflare](https://workers.cloudflare.com/built-with-cloudflare.svg)](https://tmux-tutorial-5ww.pages.dev/)

Interactive visual tutorial for tmux terminal multiplexer. Built with React + Tailwind CSS, deployed to Cloudflare Pages.

Content is in **Indonesian (Bahasa Indonesia)**.

## Sections

- **Session** — Create, list, attach, detach, kill sessions
- **Window** — Create, rename, switch, close windows
- **Pane** — Split vertical/horizontal, multi-split, close panes
- **Navigasi** — Arrow keys, pane numbers, window/session switching
- **Resize** — Resize panes, zoom/fullscreen toggle, auto layouts
- **Copy Mode** — Scroll, search, select, copy, paste terminal output

Each section includes a shortcut reference table and an interactive terminal demo.

## Tech Stack

- **Frontend:** React 19 + Vite 6
- **Styling:** Tailwind CSS v4 + shadcn/ui (dark theme)
- **Fonts:** Inter (sans) + JetBrains Mono (mono)
- **Deploy:** Cloudflare Pages via GitHub Actions

## Development

```bash
npm install
npm run dev       # Vite dev server
npm run build     # Production build → dist/
npm run preview   # Preview production build locally
```

## Deployment

Deploys automatically to Cloudflare Pages on push to `main` via GitHub Actions.

**Required GitHub Secrets:**
- `CLOUDFLARE_API_TOKEN` — API token with Cloudflare Pages edit permission
- `CLOUDFLARE_ACCOUNT_ID` — Your Cloudflare account ID

## Origin

Extracted from [tmux-api](https://github.com/onchainyaotoshi/tmux-api) frontend (`/about-tmux` page) into a standalone static site.

## License

MIT
