# qss20-final-project
**Author:** Randy Liu  
**Course:** QSS 20, Dartmouth College, Spring 2026

## Live Site
https://randyliu078-bit.github.io/qss20-final-project/

## Project Summary
This project builds a merged dataset from three federal sources. The first is the 
LEHD Post-Secondary Employment Outcomes (PSEO), which tracks earnings and employment 
for college graduates by institution and field of study. The second is the ACS Public 
Use Microdata Sample (PUMS), which provides individual-level Census records on 
education, occupation, and earnings. The third is the BLS Quarterly Census of 
Employment and Wages (QCEW), which reports county-level employment counts and wages 
by industry. Together these sources support an analysis of college-educated labor 
markets in Connecticut relative to Greater Boston (MA) and New York City (NY).

The project addresses two interrelated questions. First, it examines the stock-flow 
gap: whether Connecticut produces more bachelor's degrees (the flow) than it retains 
as college-educated residents in its workforce (the stock). A state in this position 
is considered a net exporter of educated labor. Second, it tests whether places with 
a higher share of college-degree holders generate positive spillover effects for 
workers without four-year degrees. These spillovers are measured through average weekly wages at the county level, using QCEW wage data merged with ACS degree-share estimates. Special attention is given to STEM graduates and 
the aerospace and advanced manufacturing industries, which represent a significant 
share of Connecticut's regional economy.
## Data Sources
- **PSEO** — LEHD Post-Secondary Employment Outcomes (graduate flow by state)
- **ACS PUMS** — American Community Survey microdata (resident stock, degree share)
- **QCEW** — BLS Quarterly Census of Employment and Wages (county-level wages)

Data is pulled directly from public APIs at runtime. Sources:
- ACS: https://api.census.gov/data/
- QCEW: https://data.bls.gov/cew/data/api/
- PSEO: https://lehd.ces.census.gov/data/pseo/R2024Q4/
  
## Scripts

| File | Inputs | What it does | Outputs |
|------|--------|--------------|---------|
| [`code/01_data_pull.ipynb`](code/01_data_pull.ipynb) | Census API key, PSEO LEHD URLs, BLS QCEW API | Downloads raw ACS, PSEO flows/earnings files, and QCEW county files for CT, MA, NY | Raw CSVs |
| [`code/02_clean.ipynb`](code/02_clean.ipynb) | Raw CSVs from data pull | Cleans and preps all three datasets; drops suppressed cells; constructs retention rate and wage variables | Cleaned dataframes used in analysis |
| [`code/03_analysis.ipynb`](code/03_analysis.ipynb) | Cleaned dataframes, Census API key | Produces all figures; computes retention rates, OLS regression, PUMA scatter | Figure PNGs saved to `output/` |

## Output
See `output/` for figures generated from the analysis.
