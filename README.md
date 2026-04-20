# Tekto Ltd — Holding site

A simple, static holding page for [tekto.uk](https://tekto.uk) — Tekto Ltd, a UK digital
consultancy for mobile apps, websites and smart-home solutions.

## Files

```
.
├── index.html          # Holding page
├── styles.css          # Styling (matches the brand colour theme)
└── assets/
    ├── logo.svg / .png         # Primary logo (dark backgrounds / the website)
    ├── logo-light.svg / .png   # Invoice-friendly logo (for light backgrounds)
    ├── logo-mark.svg / .png    # Icon-only "T" mark (social avatars, etc.)
    └── favicon.svg             # Browser tab icon
```

The `.png` versions are included for invoicing tools that don't accept SVG. Regenerate
them any time with:

```bash
qlmanage -t -s 2048 -o assets assets/logo.svg assets/logo-light.svg
qlmanage -t -s 1024 -o assets assets/logo-mark.svg
# qlmanage writes <name>.svg.png — rename if desired
```

## Local preview

```bash
python3 -m http.server -d . 8080
# then open http://localhost:8080
```

## Brand palette

- Teal (light) `#35E8AD`
- Teal (dark)  `#14B887`
- Blue (light) `#2F8FD8`
- Blue (dark)  `#1E6FBD`
- Background   `#0B1014`

## Deploy

It's plain HTML/CSS — drop the folder onto any static host (Cloudflare Pages, GitHub
Pages, Netlify, S3, etc.).

Clone:

```bash
git clone git@github.com:alantouk/TekTo.git
cd TekTo
```

## License

TBD.
