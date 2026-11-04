# India Literacy Intelligence Dashboard

Static GitHub Pages project for exploring Indian literacy data.

## Current build
- India-wide PLFS 2025 headline literacy rate: 81.1% (age 7+).
- State/UT PLFS 2025 literacy estimates split by rural, urban and combined residence.
- Male, female and persons rates, with gender-gap calculations.
- Interactive charts, residence/gender selectors and state search.
- Official sources and methodology notes.

## Data files
- `data/plfs_2025_total.csv`
- `data/plfs_2025_rural.csv`
- `data/plfs_2025_urban.csv`
- `data/metadata.json`

## Planned next stages
1. Add Census 2011 state and district population/literate/illiterate counts.
2. Add Census C-08 age cohorts by sex and residence.
3. Add state population rankings, literate/illiterate population rankings and state explorer.
4. Add India map and historical comparison series with methodology warnings.
5. Add metro/city analysis using Census city tables, explicitly marked Census 2011.

## Deploy to GitHub Pages
1. Create a public repository named `india-literacy-dashboard` under `aniketverse`.
2. Upload the contents of this folder to the repository root (not the folder itself).
3. In Settings → Pages, select Deploy from a branch, `main`, folder `/ (root)`.
4. Save. The site should appear at `https://aniketverse.github.io/india-literacy-dashboard/`.

## Important methodology
PLFS 2025 rates are survey estimates, not Census counts. Census 2011 counts and age cohorts are separately labelled. Never infer current population counts by multiplying PLFS rates by Census 2011 population. Metro/semi-urban is not a separate PLFS literacy category.
