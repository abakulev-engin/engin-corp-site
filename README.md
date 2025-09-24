[README.md](https://github.com/user-attachments/files/22505208/README.md)
# Eng.In Corp — Website

This repo hosts the Eng.In Corp one-page site.

## Files
- `index.html` — the website (root of repo)
- `CNAME` — custom domain: `www.engincorp.com` (already provided)

## Enable GitHub Pages
1. Repo → **Settings → Pages**.
2. **Source**: *Deploy from a branch*.
3. **Branch**: `main` and **/ (root)** → **Save**.
4. In **Settings → Pages**, set **Custom domain** to **www.engincorp.com** → **Save**.
5. Enable **Enforce HTTPS** once available.

## DNS (at your registrar, e.g., GoDaddy)
- **CNAME** record for **Host** `www` → **Value** `YOUR_GITHUB_USERNAME.github.io`
  - Example: `alexbakulev.github.io` (no `https://`, no slashes).
- **A** records for **Host** `@` → these four GitHub Pages IPs:
  - `185.199.108.153`
  - `185.199.109.153`
  - `185.199.110.153`
  - `185.199.111.153`

> Do **not** delete MX/SPF/DKIM/DMARC records for email. Only adjust A/CNAME for the website.

## Verify DNS (any terminal)
```bash
dig www.engincorp.com CNAME +short   # expect: YOUR_GITHUB_USERNAME.github.io.
dig engincorp.com A +short           # expect: 4 IPs above
```

_Updated 2025-09-24_
