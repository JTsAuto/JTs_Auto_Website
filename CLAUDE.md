# JTs Auto Website

Static site (HTML + `style.css`) deployed via Cloudflare Workers. Brand colors and fonts come from the vault note `Branding/Brand Colors and Fonts.md`.

## Workflow
`main` is locked down and deploys production; `dev` is the long-lived working branch (keep it, never delete it).
1. Work on `dev` (or a short branch off it) and push.
2. Check changes on the dev URL: https://dev-jts-auto-website.car9000knox.workers.dev
3. Open a PR from `dev` to `main` and merge it. Cloudflare deploys production.
4. **Sync after every merge:** `git checkout dev && git pull origin main && git push origin dev`
