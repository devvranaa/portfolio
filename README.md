# Portfolio

Single page student developer portfolio. Built with Astro + Tailwind v4. Static output, deploys anywhere.

## Run it

```bash
npm install
npm run dev
```

Build:

```bash
npm run build
```

## Change the name and links

One file: `src/data/site.ts`. Name, email, GitHub, project URLs. Everything on the page reads from it.

## Add a project later

Create one markdown file in `src/content/projects/`, for example `my-second-build.md`:

```md
---
title: "My second build"
tagline: "One line about what it is."
stack: ["TypeScript", "React"]
liveUrl: "https://example.com"
repoUrl: "https://github.com/you/repo"
featured: true
order: 2
coverSeed: "my-second-build"
---

## What it is
...
```

It appears on the page automatically. No code changes. Set `featured: false` to hide it without deleting it.

## Images still needed (placeholders are live right now)

All current images are random placeholders. Replace before showing anyone who matters:

1. Hero: `src/components/Hero.astro`, picsum seed `training-ground`. Use a real photo or a game screenshot, 960x720.
2. Case study cover: `src/content/projects/guess-pl-footballer.md`, `coverSeed`. Use 2 real game screenshots at 1200x900, saved to `public/images/`, referenced directly.

## Deploy on Vercel

1. Push this folder to GitHub.
2. Vercel dashboard: Add New Project, import the repo.
3. Framework preset: Astro. Build command `npm run build`, output `dist`. Defaults work.
4. Done. Every push redeploys.
