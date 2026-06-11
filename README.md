# Upstream Initiative — Website

Static multi-page site for Upstream Initiative LLC. No backend, no build step, no database.
Total size ~760KB. Just static HTML + image assets.

## Pages
- `index.html` — landing page (parent brand, app cards, contact)
- `approach.html` — The Upstream Approach info page → Contact
- `growaware.html` — GrowAware info page (marked "Publishing shortly") → Contact
- `assets/` — logos

## Deploy options (all free, no storage limit)

### Option A — Vercel (recommended; you already use it for GrowAware)
1. Put this folder in a GitHub repo (e.g. `upstream-initiative-site`).
2. In Vercel: New Project → import the repo.
3. Framework preset: **Other** (it's plain static — no build command, output dir = root).
4. Deploy. You'll get a `*.vercel.app` URL.
5. Add your domain: Vercel project → Settings → Domains → add `upstreaminitiative.org`.
6. In Northwest (your registrar), point the domain's DNS to Vercel
   (Vercel shows the exact records — usually an A record or a CNAME).

### Option B — drag-and-drop (no GitHub)
- Vercel and Cloudflare Pages both let you drag this folder in to deploy. No repo needed.

## To update later
- Edit the HTML, push to GitHub (or re-drag the folder). Live in seconds.

## When you start billing / fundraiser (later)
- Add a serverless function (Vercel `api/` folder, like GrowAware) for Stripe or a donation flow.
- Swap the GrowAware "Publishing shortly" badge / button for the live link or donate link.
- The static pages stay as-is; you only add the backend piece when money flows through it.

## Notes
- Contact is a `mailto:` link to upstreaminitiative@outlook.com — no form backend needed.
- Neither app links directly into the live app (by design):
  - Approach is deployed agency-by-agency → routes to contact.
  - GrowAware is held for a possible fundraiser → "Publishing shortly" → routes to contact.
