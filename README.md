# Electronics Dokan Static Storefront

This is a database-free static catalogue for GitHub Pages. Product data lives in `data/products.json`, site settings in `config/site.json`, and image mappings in `data/image-manifest.json`.

## Local preview

Run any static server from this directory, for example:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Images

Rename product images exactly as listed in `IMAGE_UPLOAD_GUIDE.md` and upload them to `assets/products/`. The site resolves variant image → parent image → local placeholder. Missing filenames are logged in the browser console.

## GitHub Pages

Enable Pages from the repository's Settings → Pages. The included workflow deploys the repository root using GitHub Pages. The `CNAME` file is configured for `electronicsdokan.store`.

## Namecheap DNS setup

At Namecheap Advanced DNS, after switching from the old custom DNS provider to Namecheap BasicDNS, create these records:

| Type | Host | Value | TTL |
|---|---|---|---|
| A | @ | 185.199.108.153 | Automatic |
| A | @ | 185.199.109.153 | Automatic |
| A | @ | 185.199.110.153 | Automatic |
| A | @ | 185.199.111.153 | Automatic |
| CNAME | www | cn316240bd.github.io | Automatic |

Review and preserve any required MX/TXT records before replacing DNS.
