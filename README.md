# nujoomona-website

Static site for [nujoomona.com](https://nujoomona.com): home page, privacy policy and terms of service (needed for the YouTube API audit).

## Layout

- `public/` is the site root (plain HTML + CSS, no build step).

## Deploy (Cloudflare Pages)

Manual upload: Workers & Pages → Create → Pages → Upload assets, then upload the `public/` folder.

Or with Wrangler:

```sh
npx wrangler pages deploy public --project-name nujoomona
```

Once the repo is on GitHub, connect it in Cloudflare Pages (build command: none, output directory: `public`) so every push to `main` deploys.
