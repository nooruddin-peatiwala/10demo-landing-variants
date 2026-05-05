# 10demo · Landing-Page A/B Variants

Three landing-page redesigns of [10demo.com](https://10demo.com), built to A/B test against the live site. All three share the same copy, stats, brand colors (lavender `#7b68ee` + orange `#ea6e1b`), and section structure — only the design hypothesis differs.

## Live URLs

Each URL serves only one variant — no switcher visible to end users, no signal that alternatives exist.

| | Variant | Hypothesis | URL |
|---|---|---|---|
| **A** | Outcome-Led | B2B buyers convert faster when they see the dollar outcome up front, not a clever joke. ROI is the hook. | <https://10demo-variant-a.vercel.app> |
| **B** | Product-Led | The product is visual enough that watching it sells better than reading about it. Mock chat widget in hero. | <https://10demo-variant-b.vercel.app> |
| **C** | Brand-Led | Personality and memorability beat yet-another-feature-grid. Calendar joke amplified to centerpiece. | <https://10demo-variant-c.vercel.app> |

## Repo layout

```
.
├── a/       Variant A · Outcome-Led    (Vercel project: 10demo-variant-a)
├── b/       Variant B · Product-Led    (Vercel project: 10demo-variant-b)
└── c/       Variant C · Brand-Led      (Vercel project: 10demo-variant-c)
```

Each subdir is a self-contained static site: `index.html` + `assets/brand.css` + `assets/logo.svg`. Vercel auto-detects static HTML — no build step.

## Updating

Push to `main` → all 3 Vercel projects redeploy automatically (each scoped to its own subdirectory).

## Notes

- Brand colors and copy are locked across all 3 variants by design — the A/B test isolates the design hypothesis, not styling drift.
- Source assets and brand spec live in the parent project, not committed here.
