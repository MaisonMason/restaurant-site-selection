# Restaurant Site Selection — UTC vs Convoy (San Diego)

**Course:** MGTA 452 — Customer Analytics, UC San Diego Rady School of Management (2026)  
**Tools:** Python · pandas · geopandas · matplotlib · Jupyter · Open Government Data

---

## Overview

A data-driven site selection analysis to evaluate whether opening a new **Chef Fei** restaurant in **UTC (ZIP 92122)** would outperform **Convoy (ZIP 92111)** in San Diego. Used exclusively official/public data sources for full reproducibility.

**Recommendation:** UTC — higher household income, lower restaurant density per capita, stronger liquor license penetration for the dine-in + cocktail positioning.

---

## Repository Structure

```
restaurant-site-selection/
├── chef_fei_site_selection.ipynb     # Full analysis: data pull → market sizing → recommendation
├── data/                             # Cached CSVs (open government sources)
└── README.md
```

---

## Data Sources (All Public)

| Source | Description |
|--------|-------------|
| City of San Diego Active Businesses | Restaurant count and business density by ZIP |
| California ABC Liquor Licenses | Type 41/47/48 license penetration by ZIP |
| SANDAG ZIP Demographics | Population, income, ethnicity by ZIP code |

---

## Methodology

1. **Market Sizing** — Restaurant count per 1,000 residents (competition density)
2. **Liquor License Analysis** — Penetration of full-service licenses (Type 47/48) as proxy for dine-in market maturity
3. **Demographic Profiling** — Median household income, Chinese-American population share (key customer segment for Chef Fei)
4. **Competitive Landscape** — Active restaurant count, cuisine category distribution

---

## Key Findings

| Metric | UTC (92122) | Convoy (92111) |
|--------|------------|----------------|
| Restaurants per 1K residents | Lower | Higher |
| Median household income | Higher | Lower |
| Type 47/48 license density | Comparable | Higher |
| Chinese-American share | Lower | Higher |

**Verdict:** UTC offers a less saturated market with higher income demographics, better suited for Chef Fei's dine-in + cocktail positioning. Convoy has stronger ethnic food density but higher competition for the target segment.

---

## How to Run

```bash
pip install pandas numpy matplotlib seaborn requests jupyter

jupyter notebook chef_fei_site_selection.ipynb
```

Data is fetched directly from public APIs/CSVs — no manual downloads required.

---

## Author

**Dingyi (Mason) Wang** — MSBA Candidate, UC San Diego Rady School of Management  
[LinkedIn](https://linkedin.com/in/dyw01) · [Portfolio](https://MaisonMason.github.io)
