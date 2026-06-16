# Areeb Islam — Portfolio

A modern, single-page personal portfolio built with [Astro](https://astro.build) and deployed to GitHub Pages.

**Live site:** https://are021.github.io/portfolio

## Sections

- **Hero** — intro highlighting roles as a Software Engineer at Meta and a freelance software developer
- **Experience** — Freelance, Meta, and General Motors
- **Projects** — award-winning hackathon projects with tech tags
- **Skills** — curated languages, frameworks, and tools
- **Education & Research** — Michigan State University degree and research assistant work

All content lives in the frontmatter arrays at the top of `src/pages/index.astro` — edit those objects to update the site.

## Develop locally

This project requires **Node ≥ 22.12** (see `package.json` engines).

```sh
nvm use 22      # or otherwise ensure Node 22+
npm install
npm run dev     # http://localhost:4321/portfolio
```

| Command           | Action                                       |
| :---------------- | :------------------------------------------- |
| `npm run dev`     | Start the local dev server                   |
| `npm run build`   | Build the production site to `./dist/`       |
| `npm run preview` | Preview the production build locally         |

## Deploy to GitHub Pages

Deployment is automated via GitHub Actions (`.github/workflows/deploy.yml`).

1. Push this project to a GitHub repo named **`portfolio`** under the `are021` account.
2. In the repo, go to **Settings → Pages → Build and deployment** and set **Source** to **GitHub Actions**.
3. Push to the `main` branch. The workflow builds the site and publishes it to
   https://are021.github.io/portfolio.

### Using a root user site instead

If you'd rather serve the site at `https://are021.github.io` (no `/portfolio` path):

1. Rename the repo to `are021.github.io`.
2. In `astro.config.mjs`, change `base` to `'/'` (keep `site: 'https://are021.github.io'`).

### Custom domain

Add a `public/CNAME` file containing your domain, set `site` to that domain and
`base` to `'/'` in `astro.config.mjs`, and configure the domain under Settings → Pages.
