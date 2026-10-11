# nujoomona-website

Static site for [nujoomona.com](https://nujoomona.com): home page, privacy policy and terms of service (needed for the YouTube API audit).

## Layout

- `public/` is the site root (plain HTML + CSS, no build step).

## Deploy (Cloudflare Workers static assets)

The repo is connected to Cloudflare Workers Builds: every push to `main` runs `npx wrangler deploy`, which serves `public/` as static assets using `wrangler.jsonc` (unknown paths get `public/404.html`).

To deploy by hand:

```sh
npx wrangler deploy
```
