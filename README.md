# SISKM

Static website for SISKM. Built for [Cloudflare Pages](https://developers.cloudflare.com/pages/).

## Local

```bash
python3 -m http.server -d public 8080
```

Open http://localhost:8080

## Deploy on Cloudflare Pages

1. In the Cloudflare dashboard, go to **Workers & Pages** → **Create** → **Pages** → **Connect to Git**.
2. Select the `siskm-website` repository.
3. Use these build settings:

| Setting | Value |
| --- | --- |
| Framework preset | None |
| Build command | *(leave empty)* |
| Build output directory | `public` |

4. Deploy. Later pushes to `main` will publish automatically.

Direct upload without Git:

```bash
npx wrangler pages deploy public --project-name=siskm-website
```
