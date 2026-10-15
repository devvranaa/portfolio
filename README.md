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
cover: "https://images.unsplash.com/photo-XXXX?q=80&w=1200&auto=format&fit=crop"
coverAlt: "Describe the image in one line"
---

## What it is
...
```

It appears on the page automatically. No code changes. Set `featured: false` to hide it without deleting it.

## Images

Hero and project covers are topical stock photos (Unsplash CDN) with honest alt text. They hold up, but real game screenshots are stronger. When ready, save them to `public/images/` and point the `cover` field (in the project markdown) or the hero `img` (in `src/components/Hero.astro`) at the local file.

## Deploy on Vercel

1. Push this folder to GitHub.
2. Vercel dashboard: Add New Project, import the repo.
3. Framework preset: Astro. Build command `npm run build`, output `dist`. Defaults work.
4. Done. Every push redeploys.
