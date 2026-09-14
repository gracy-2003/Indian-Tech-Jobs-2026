# Indian Tech Jobs 2026 — Market Analytics Dashboard

End-to-end analysis of the Indian tech hiring market: **23,201 raw job listings** cleaned in Python, analysed in MySQL, and delivered as a 5-page interactive Power BI report answering where the jobs are, who is hiring, what they pay, and which skills they ask for.

**Stack:** Python (Pandas, NumPy, Matplotlib, Seaborn) · MySQL · Power BI (DAX, Data Modeling) · Excel

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

## Dashboard pages

1. **Executive Dashboard** — headline KPIs: total listings, companies hiring, median salary, remote share
2. **Company** — top hiring companies, listings per company, company ratings vs. hiring volume
3. **Location** — city-level listing counts and pay comparison
4. **Salary** — salary distribution by tier, experience band, city and work mode
5. **Skills & Roles** — most in-demand skills and role families, and how they map to pay

## Key findings

- **TCS, Accenture and EY** lead hiring volume among the 3,225+ companies in the dataset.
- Salary varies sharply by **city** and by **experience band** — the two strongest levers in the data, ahead of company rating.
- **Work mode** (remote / hybrid / onsite) splits the market unevenly across cities, so "remote-friendly" is a local phenomenon rather than a national one.
- A concentrated set of **in-demand skills** recurs across the top-paying listings, giving candidates a clear prioritisation order.

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

**Author:** Gracy Srivastava — Data Analyst (SQL · Power BI · Python)
[LinkedIn](https://www.linkedin.com/in/gracy2003) · [GitHub](https://github.com/gracy-2003)
