# Indian Tech Jobs 2026 — Market Analytics Dashboard

![Python](https://img.shields.io/badge/Python-Pandas%20%7C%20NumPy%20%7C%20Seaborn-3776AB?logo=python&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-CTEs%20%7C%20Window%20Functions-4479A1?logo=mysql&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-DAX%20%7C%20Data%20Modeling-F2C811?logo=powerbi&logoColor=black)
![Excel](https://img.shields.io/badge/Excel-Power%20Query-217346?logo=microsoftexcel&logoColor=white)

End-to-end analysis of the Indian tech hiring market: **23,201 raw job listings** cleaned in Python, analysed in MySQL, and delivered as a 5-page interactive Power BI report answering where the jobs are, who is hiring, what they pay, and which skills they ask for.

**Stack:** Python (Pandas, NumPy, Matplotlib, Seaborn) · MySQL · Power BI (DAX, Data Modeling) · Excel

| At a glance | |
|---|---|
| **Raw listings processed** | 23,201 |
| **Curated analysis set** | 9,010 listings |
| **Derived features engineered** | 13 |
| **Companies covered** | 3,225+ |
| **Cities covered** | 11 major Indian cities |
| **Report pages** | 5 |

---

## Problem

Job-market data for Indian tech roles is scattered, inconsistently formatted, and full of free-text salary and location fields — which makes it useless for answering the questions a candidate or a recruiter actually cares about:

- Which companies are hiring at volume, and for what?
- Which cities pay the most, and how does that change with experience?
- How much of the market is genuinely remote versus hybrid or onsite?
- Which skills appear most often in the highest-paying listings?

## What I built

| Stage | What happened |
|---|---|
| **Ingest & clean** | Parsed and standardised **23,201 raw listings** in Python/Pandas — deduplication, salary string parsing, location normalisation, null handling |
| **Feature engineering** | Engineered **13 derived features**: salary tiers, experience bands, remote/hybrid/onsite work-mode flags, top-city indicator, top-rated-company indicator, and more |
| **SQL analysis** | Loaded a curated **9,010-listing** analysis set into MySQL and wrote queries using **CTEs, window functions, GROUP BY and aggregate functions** to profile hiring and salary trends across **3,225+ companies** and **11 major Indian cities** |
| **Visualisation** | Built a **5-page Power BI report** with DAX measures, cross-page slicers, bar/donut charts and treemaps |

## Dashboard preview

**Executive Dashboard** — headline KPIs: total listings, companies hiring, median salary, remote share

![Executive Dashboard](Outputs/Executive%20Dashboard.png)

**Company Analysis** — top hiring companies, listings per company, company ratings vs. hiring volume

![Company Analysis](Outputs/Company%20Analysis.png)

**Location Analysis** — city-level listing counts and pay comparison

![Location Analysis](Outputs/Location%20Analysis.png)

**Salary Analysis** — salary distribution by tier, experience band, city and work mode

![Salary Analysis](Outputs/Salary%20Analysis.png)

**Skills & Job Roles** — most in-demand skills and role families, and how they map to pay

![Skills and Job Roles](Outputs/Skills%20%26%20Job%20Roles.png)

## Key findings

- **TCS, Accenture and EY** lead hiring volume among the 3,225+ companies in the dataset.
- Salary varies sharply by **city** and by **experience band** — the two strongest levers in the data, ahead of company rating.
- **Work mode** (remote / hybrid / onsite) splits the market unevenly across cities, so "remote-friendly" is a local phenomenon rather than a national one.
- A concentrated set of **in-demand skills** recurs across the top-paying listings, giving candidates a clear prioritisation order.

## Skills demonstrated

| Area | Applied here |
|---|---|
| **Advanced SQL** | CTEs, window functions, joins, `GROUP BY`, aggregate functions, query optimization (MySQL) |
| **Python** | Pandas, NumPy, Matplotlib, Seaborn — cleaning, wrangling, feature engineering, EDA |
| **BI & Visualization** | Power BI — DAX measures, data modeling, slicers, bar/donut charts, treemaps |
| **Data Engineering** | ETL pipeline: raw .xls to cleaned dataset to curated analysis set to BI import layer |
| **Analysis** | Distribution and outlier review, segment comparison, salary driver analysis |

## Repository structure

```
Indian-Tech-Jobs-2026/
├── 01_Data_Cleaning.ipynb              # Raw ingest, dedup, salary/location parsing
├── 02_Exploratory_Data_Analysis.ipynb  # Distributions, trends, outlier review
├── 03_Feature_Engineering.ipynb        # 13 derived features for modelling & BI
├── Indian Tech Jobs 2026.pbix          # 5-page Power BI report
├── indian_tech_jobs_2026.xls           # Raw dataset (23,201 listings)
├── cleaned_indian_tech_jobs.xls        # Post-cleaning dataset
├── final_jobs_dataset.csv / .xls       # Curated analysis set (9,010 listings)
├── jobs_ready_for_powerbi.xls          # Power BI import layer
└── Outputs/                            # Dashboard screenshots & exports
```

## How to run it

1. Open the notebooks in order (`01` → `02` → `03`) with Jupyter; they need `pandas`, `numpy`, `matplotlib` and `seaborn`.
2. Load `final_jobs_dataset.csv` into MySQL to reproduce the SQL analysis layer.
3. Open `Indian Tech Jobs 2026.pbix` in Power BI Desktop and point the data source at `jobs_ready_for_powerbi.xls`.

---

**Author:** Gracy Srivastava — Data Analyst (SQL · Power BI · Python) · B.Tech CSE, 2026
[LinkedIn](https://www.linkedin.com/in/gracy2003) · [GitHub](https://github.com/gracy-2003) · gracysrivastava2003@gmail.com
