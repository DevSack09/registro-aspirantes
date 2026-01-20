# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Commands

```bash
npm run dev       # Start dev server at localhost:4321
npm run build     # Build for production to ./dist/
npm run preview   # Preview production build locally
```

## Architecture

This is an **Astro 5** project with **Tailwind CSS 4** (via Vite plugin).

### Project Structure

- `src/pages/` - File-based routing. Each `.astro` file becomes a route
- `src/layouts/` - Page layouts wrapping content via `<slot />`
- `src/components/` - Reusable Astro components
- `src/assets/` - Images/assets processed by Astro's build pipeline
- `src/styles/global.css` - Global styles with Tailwind import
- `public/` - Static assets served directly (not processed)

### Tech Stack

- **Astro** handles SSG/SSR and component rendering
- **Tailwind CSS** configured in `astro.config.mjs` via `@tailwindcss/vite` plugin
- **TypeScript** with strict mode (`astro/tsconfigs/strict`)
