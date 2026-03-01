# Cordell's homepage

## Quick Reference

```bash
make              # Start local dev server at http://127.0.0.1:8000/
```

## Architecture

Minimal personal homepage — everything is in `index.html` (HTML + CSS inline). No build step, no bundler, no package manager, no external dependencies. Deployed via GitHub Pages from `main` branch, proxied through Cloudflare.

### Key Files

- `index.html` — The entire site
- `serve` — Python HTTP server for local dev
- `CNAME` — GitHub Pages custom domain (`cblakkan.com`)
- `favicon.ico` — Site icon

## Deployment

Push to `main` → GitHub Pages auto-deploys → Cloudflare proxies traffic.

DNS is managed in Cloudflare:
- A records for `cblakkan.com` → GitHub Pages IPs
- CNAME `www` → `cblakkan.github.io`
- SSL/TLS mode: **Full** (not Flexible)
