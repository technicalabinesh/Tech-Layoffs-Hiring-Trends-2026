# Tech Layoffs & Hiring Trends (2024–2026)

## Executive Summary

This repository presents an exploratory data analysis (EDA) project focused on global technology-sector layoffs and hiring trend signals across **2024, 2025, and 2026**.  
The goal is to convert raw event-level workforce data into actionable intelligence for founders, HR leaders, investors, and analysts who need to understand:

- where workforce reductions are concentrated,
- which industries and geographies are most volatile,
- how layoff reasons evolve over time,
- and what patterns can inform strategic workforce planning.

The project combines a structured CSV dataset with a reproducible Jupyter Notebook workflow to profile data quality, summarize distributions, inspect trend behavior, and surface business-facing insights.

---

## Project Objectives

This analysis is designed to answer high-impact workforce questions:

1. **Scale and concentration**  
   How large is the layoff volume, and where is it concentrated by company, industry, country, and firm size?

2. **Temporal behavior**  
   Are there seasonal patterns or year-to-year shifts in layoffs?

3. **Root-cause perspective**  
   Which reasons (AI automation, restructuring, cost cutting, market slowdown, overhiring correction) are most associated with larger workforce reductions?

4. **Decision support**  
   What can decision-makers use from this data for hiring strategy, risk planning, and organizational resilience?

---

## Repository Contents

```text
.
├── README.md
├── LICENSE
├── Tech_Layoffs_Hiring_Trends_EDA (1).ipynb
└── tech_layoffs_hiring_trends_elite_v2-selected-columns (1).csv
```

- **`Tech_Layoffs_Hiring_Trends_EDA (1).ipynb`**: Main notebook for end-to-end analysis.
- **`tech_layoffs_hiring_trends_elite_v2-selected-columns (1).csv`**: Source dataset used in the notebook.

---

## Dataset Overview

The dataset contains **12,000 records** and **10 columns**, where each row represents a company layoff event snapshot:

| Column | Description |
|---|---|
| `record_id` | Unique identifier for each record |
| `company_name` | Company associated with the layoff event |
| `industry` | Industry segment (e.g., AI, Cloud, FinTech) |
| `country` | Country linked to the company/event |
| `company_size` | Size category (Startup, Mid-size, Enterprise, Big Tech) |
| `month` | Month of the event |
| `year` | Year of the event (2024–2026) |
| `layoffs_count` | Number of layoffs in the event |
| `layoff_percentage` | Workforce percentage impacted |
| `reason_for_layoffs` | Stated primary reason |

### Snapshot Metrics

- **Total layoffs represented**: 60,114,865  
- **Average layoffs per record**: 5,009.57  
- **Median layoffs per record**: 2,733  
- **Max layoffs in a single record**: 19,999  
- **Average layoff percentage**: 12.78%

---

## Analysis Workflow

The notebook follows a practical EDA pipeline:

1. **Dataset Overview**  
   Shape, schema, and data types.

2. **Data Quality Checks**  
   Missing values, duplicates, and type sanity.

3. **Descriptive Statistics**  
   Numeric summaries and categorical cardinality.

4. **Distribution Analysis**  
   Histograms and boxplots for numeric indicators.

5. **Categorical Analysis**  
   Frequency and concentration across companies, countries, industries, sizes, and reasons.

6. **Correlation Analysis**  
   Numeric relationships between layoff indicators.

7. **Date/Time Analysis**  
   Year and month trend decomposition.

8. **Outlier Analysis**  
   IQR-based checks for extreme layoff records.

9. **Business Questions Layer**  
   A strategic interpretation section to transition from charts to decisions.

10. **Automated EDA Summary**  
    Consolidated narrative output for quick review.

---

## Key Findings (Current Dataset Pass)

### 1) Yearly layoff totals are consistently high
- 2024: **20,307,870**
- 2025: **19,761,032**
- 2026: **20,045,963**

Interpretation: layoffs remain elevated across all three years rather than being a one-time spike.

### 2) Industry impact is broad, not isolated
Highest cumulative layoff volumes appear in:
- Social Media
- AI
- E-Commerce
- Cybersecurity
- Gaming

Interpretation: workforce pressure spans both mature and growth segments.

### 3) Drivers are multi-causal
Top reasons by aggregate layoff volume:
- AI Automation
- Restructuring
- Cost Cutting
- Market Slowdown
- Overhiring Correction

Interpretation: layoffs are linked to both technology transformation and classic business-cycle pressures.

### 4) Geographic pressure is distributed
Largest cumulative layoff counts are observed across the UK, Singapore, USA, Canada, India, and Germany.

Interpretation: this is a multi-region phenomenon, not a single-market correction.

### 5) Seasonality signal appears in monthly totals
Month-level variation indicates recurring waves, with some months showing noticeably higher totals than others.

Interpretation: planning annual hiring/freeze cycles around seasonal volatility may reduce organizational risk.

---

## How to Run the Analysis

### Prerequisites
- Python 3.9+
- Jupyter Notebook / JupyterLab

### Recommended setup

```bash
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\\Scripts\\activate
pip install pandas numpy matplotlib jupyter
```

### Launch notebook

```bash
jupyter notebook
```

Open:

`Tech_Layoffs_Hiring_Trends_EDA (1).ipynb`

and run all cells in order for a full reproducible pass.

---

## Intended Use Cases

- **Executive planning**: workforce risk and hiring cadence calibration  
- **People analytics**: regional and industry benchmarking  
- **Investment research**: sector resilience and operational discipline signals  
- **Career intelligence**: identifying relatively stable or high-volatility areas

---

## Limitations and Interpretation Notes

- The dataset should be interpreted as an analytic training/insight asset unless externally validated as authoritative ground truth.
- Layoff events are represented at record level; avoid over-generalizing individual company behavior without additional context.
- Causal claims should be tested with complementary macroeconomic, funding, and revenue data.

---

## Next Enhancements

- Add interactive dashboards (Plotly/Power BI/Tableau export pipeline)
- Add year-over-year and month-over-month delta tables
- Add confidence flags and anomaly detection layers
- Add predictive scenario modeling for workforce planning

---

## License

This repository is distributed under the license terms in the `LICENSE` file.