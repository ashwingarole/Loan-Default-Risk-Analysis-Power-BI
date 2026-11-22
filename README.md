# Loan Default Risk Analysis Dashboard (Power BI)

## Project Overview
An end-to-end **BFSI Credit & Risk Analytics** dashboard built in Power BI analysing **145,326 mortgage loans** worth **$48.2 billion**, with an overall portfolio default rate of **24.61%**[cite: 1, 22]. This report helps underwriting and risk management teams pinpoint high-risk borrower segments, credit bureau anomalies, and geographic exposure.

## Dashboard Preview
![Loan Default Risk Analysis Dashboard](https://raw.githubusercontent.com/<ashwingarole>/Loan-Default-Risk-Analysis-PowerBI/main/dashboard_preview.png)

---

## Key KPIs Tracked
* **Total Loan Amount:** $48.2B[cite: 1, 22]
* **Total Loans (Count):** 145,326[cite: 1, 22]
* **Average Borrower Income:** $6,888[cite: 1, 22]
* **Overall Default Rate:** 24.61%[cite: 1, 22]
* **Average Interest Rate:** 4.04%[cite: 1, 22]

---

## Key Business Insights
* **Loan Purpose vs. Risk:** High-volume categories (**p3** at 55K loans and **p4** at 54K loans) maintain the lowest default rates (**25.01%** and **22.89%**), whereas the smallest segment (**p2** at 3K loans) exhibits the highest default risk at **33.13%**.[cite: 4, 22]
* **Credit Bureau Anomaly:** While **CIB**, **CRIF**, and **EXP** handle the majority of loan volume (40K–47K each) with low default rates (~15.8%–16.2%), **EQUI** accounts for only 15K loans yet shows a **99.99%** default rate—flagging a critical scoring anomaly.[cite: 6, 22]
* **Borrower Age Curve:** Middle-aged borrowers (**25–54**) drive the bulk of loan volume with the lowest default rates (**22.14%–23.98%**), while default risk spikes at both ends—reaching **29.02%** for borrowers under **25** and **29.90%** for seniors over **74**.[cite: 12, 22]
* **Geographic Exposure:** Over **93%** of total loan exposure is concentrated in the **North ($24.17B)** and **South ($20.90B)** regions with lower default rates (**22.46%** and **26.61%**), whereas **Central ($2.74B)** and **North-East ($0.38B)** carry higher default risk at **27.54%** and **30.21%**.[cite: 13, 14, 22]
* **Occupancy & Underwriting Tiers:** **Primary Residences** represent **93.52% ($45.05B)** of total exposure[cite: 17, 22]. Across underwriting tiers, **Non-Conforming Tier 2 (Subprime)** loans carry the highest default risk at **40.32%**, compared to **23.62%** for **Conforming Tier 1 (Prime)** loans.[cite: 22, 23]

---

## Tools & Data Preparation Techniques
* **Power BI Desktop:** Interactive visual design, dual-axis combo charts, custom KPI cards, and cross-filtering slicers (*Loan Type, Gender, Application Channel, Business vs. Commercial*)[cite: 22].
* **Power Query (ETL):** Standardised inconsistent text casing (`Region`), decoded raw categorical abbreviations (`pr`, `ir`, `sr`, `cf`, `ncf`, `l1`, `l2`), and engineered a numeric conditional sort column (`Age Sort`) to resolve chronological sorting without DAX circular dependencies[cite: 10, 11, 13, 16, 19].
* **DAX Measures:** Built custom measures for `Default Rate %` and scaled `Average Interest Rate` calculations[cite: 2].

## Dataset Source
* Kaggle: *Loan Default Dataset* (BFSI Mortgage Portfolio)
