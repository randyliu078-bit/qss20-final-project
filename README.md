# qss20-final-project
**Author:** Randy Liu  
**Course:** QSS 20, Dartmouth College, Spring 2026

## Project Summary
This project examines the stock-flow dynamics of college-educated labor in Connecticut 
relative to Greater Boston (MA) and New York City (NY), using three federal data sources. 
It tests whether Connecticut remains a net exporter of educated labor (Bound et al. 2004) 
and whether local college-degree share predicts labor-force participation for non-degree 
workers (Winters 2013).

## Data Sources
- **PSEO** — LEHD Post-Secondary Employment Outcomes (graduate flow by state)
- **ACS PUMS** — American Community Survey microdata (resident stock, degree share)
- **QCEW** — BLS Quarterly Census of Employment and Wages (county-level wages)

Data too large for repo — download links in each notebook.

## Scripts
| File | Description |
|------|-------------|
| `code/01_data_pull.ipynb` | Downloads and saves raw ACS, PSEO, QCEW data |
| `code/02_clean.ipynb` | Merges and cleans the three datasets |
| `code/03_analysis.ipynb` | Visualizations and analysis |

## Output
See `output/` for figures generated from the analysis.
