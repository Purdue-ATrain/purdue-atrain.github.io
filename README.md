# purdue-atrain.github.io

Landing page for the Purdue-ATrain organization. Live at
<https://purdue-atrain.github.io>.

## Structure

```
.
├── index.html         single-page site (Tailwind via CDN + GSAP + Mermaid)
├── assets/
│   ├── logo.png       1254×1254 brand mark
│   └── cover.png      1672×941 banner used above "Get involved"
├── benchmarks/
│   └── report.html    self-contained skill-bench dashboard (full-v03)
├── .nojekyll          disables Jekyll processing on GitHub Pages
├── LICENSE            MIT
└── README.md          this file
```

## Editing

Single HTML file. No build step. To preview locally:

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

Push to `main` and GitHub Pages redeploys in 30-60s.

## Refreshing the benchmark report

```bash
cp /path/to/atrain-skill-bench/results/<latest>/report.html benchmarks/report.html
git add benchmarks/report.html && git commit -m "benchmarks: refresh dashboard"
git push
```

## Refreshing assets

`logo.png` and `cover.png` are the brand assets. Replace in-place and push.
Optional follow-up: convert to WebP for ~70% size reduction.
