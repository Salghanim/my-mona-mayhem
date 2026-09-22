# Mona Mayhem

## Project Overview

- Mona Mayhem is an Astro site for comparing GitHub contribution graphs in a retro arcade-themed interface.
- The application lives under `src/`; `docs/` is a separate static documentation site.
- Ignore `workshop/` when changing the application. It contains instructional material only.
- The app currently uses server-side rendering with the Node standalone adapter. See [astro.config.mjs](astro.config.mjs).

## Commands

- `npm install` installs dependencies.
- `npm run dev` starts the Astro development server.
- `npm run build` creates the production server build.
- `npm run preview` serves the production build locally.
- `npm run astro` runs the Astro CLI directly.

Run `npm run build` after changes that affect pages, routes, configuration, or TypeScript.

## Astro Conventions

- Use Astro's file-based routing under `src/pages/`; dynamic route segments use bracket syntax such as `[username]`.
- Keep page/component server logic in the frontmatter block and markup in the template below it.
- Type API handlers with Astro's `APIRoute` type and export HTTP methods such as `GET` from route files.
- Preserve `prerender = false` for request-dependent API routes. The contribution endpoint is [src/pages/api/contributions/[username].ts](src/pages/api/contributions/%5Busername%5D.ts).
- Follow the strict TypeScript configuration in [tsconfig.json](tsconfig.json), and keep dependencies and scripts in [package.json](package.json).

## Deployment

- The Astro app's current `output: 'server'` configuration requires a Node-capable host.
- Do not assume the GitHub Pages workflow deploys the Astro app; deployment details and the separate static docs setup are documented in [README.md](README.md).