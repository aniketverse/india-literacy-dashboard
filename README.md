# India Literacy Intelligence Dashboard — Version 2

## Deployment
Upload/replace `index.html` in the repository root and upload the complete `data/` folder contents to the repository's `data/` folder. Keep GitHub Pages set to `main` branch and `/ (root)`.

## Files
- `index.html`: four-section responsive dashboard.
- `data/plfs_2025_total.csv`, `data/plfs_2025_rural.csv`, `data/plfs_2025_urban.csv`: PLFS 2025 state/UT estimates from the starter build.
- `data/census2011_dashboard.json`: dashboard-ready summaries from C-08, C-13 Appendix A and PCA.
- `data/census2011_state_district.csv`: district-level PCA extract.
- `data/metadata.json`: original PLFS metadata.

## Dashboard sections
1. Latest estimates: PLFS 2025.
2. Census overview: national counts, rural/urban rates, state rankings.
3. District explorer: state, residence and district filters.
4. Age & education: C-13 single-year age records aggregated into age bands, plus C-08 educational attainment.

## Methodology
- PLFS 2025 and Census 2011 are kept in separate tabs because they are different statistical products and reference periods.
- Census literacy rates use literates divided by population aged 7+.
- PCA `TOT_P - P_06` is used for population aged 7+; male/female denominators are calculated separately.
- District rankings use PCA district rows; Census 2011 is historical.
- C-13 age bands are aggregated from ages 7–99 plus the explicit 100+ category. The 60+ band includes the source's 100+ group; age not stated is excluded.
- Educational attainment chart uses C-08 category counts for the India Total / All ages row. It represents the distribution of literates by highest reported educational category, not a modern qualification equivalency.
- Metro/semi-urban categories are not inferred from these datasets.

## Sources
MoSPI PLFS 2025 Annual Report, Table 7; Census of India 2011 PCA, C-08 and C-13 Appendix A.


## Version 3 visual improvements
- Refined visual system: gradient hero, layered page background, improved card depth, spacing and typography.
- Added a state literacy tile-map view with colour bands. This is a schematic comparison grid, not a geographic boundary map; the dashboard labels it accordingly.
- Expanded state ranking metrics to include literate population, illiterate population and total population in addition to literacy rates and gender gap.


## Version 4 — Futuristic visual refresh
- Dark navy / deep-space interface with cyan, teal, electric blue and violet accents.
- Glass-style panels, subtle grid treatment, glowing interactive state tiles and hover motion.
- Plotly charts now use transparent dark canvases, brighter colour palette, cleaner gridlines and custom hover labels.
- Fixed the state tile map rendering call so the map actually populates on the Census overview tab.
- All original PLFS and Census data files remain unchanged.


## Version 5 — Geographic exploration
- Added a true clickable India state-boundary choropleth (not a tile grid).
- State polygons are shaded by selected Census 2011 indicator: overall, male/female literacy, gender gap, literate or illiterate population.
- Clicking a state loads its district boundary layer and joins Census 2011 PCA district records by normalized district name.
- Boundary data is fetched on demand from Hari31416/india-geojson-assets (versioned display GeoJSON; see repository README for source details). District boundaries may reflect a different administrative vintage than Census 2011. Unmatched newer/renamed districts are left uncoloured; the table remains the authoritative Census 2011 record.
- Map boundary files are fetched from the external repository at runtime to keep this GitHub Pages package lightweight. Internet access is required for the geographic layer.
