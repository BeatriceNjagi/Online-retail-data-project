# Online Retail Data Analysis — Python & SQL

An end-to-end data analysis project covering data ingestion, cleaning, SQL storage, and business insight generation using a publicly available online retail dataset.

---

## Project Overview

This project analyses transactional retail data to answer key business questions around revenue performance, customer behaviour, and global product demand. The workflow follows a full data pipeline — from raw data loading through to cleaned analysis and insights.

---

## Tools Used

- **Python** — data ingestion, cleaning, and analysis
- **Pandas** — data manipulation and transformation
- **PostgreSQL** — data storage and querying
- **SQLAlchemy** — connecting Python to the SQL database

---

## Project Phases

### Phase 1 — Data Ingestion

Loaded the raw Excel dataset into Python and performed an initial inspection:

- Reviewed structure using `.head()`, `.shape()`, `.describe()`, and `.info()`
- Confirmed correct data types across all fields

---


### Phase 2 — Data Cleaning & Transformation $ Data Storage (SQL Layer)

Cleaned the raw data to ensure accuracy and consistency:

| Issue | Action Taken |
|---|---|
| Negative or zero quantities | Removed |
| Negative unit prices | Removed |
| Cancelled invoices (InvoiceNo starting with "C") | Excluded |
| Missing CustomerID | Rows dropped |
| Duplicate records | Removed |

- Both raw and cleaned datasets were stored as separate SQL tables for transparency and reproducibility.
- Verified table creation, data types, and row counts


---

## Analysis & Key Findings

### 1. Monthly Revenue Performance (2011)

- **November** was the highest revenue month — up 12% from October, likely driven by early Christmas shopping and Black Friday promotions
- **September** recorded the largest single month-on-month increase (+48%), followed by **May** (+45%)
- **December** saw the sharpest decline (-55%), consistent with post-holiday slowdown
- Further dips were recorded in **February** and **April** (both -21%)

### 2. Country Performance (Excluding UK)

- **Top markets by revenue:** Netherlands, Eire, Germany
- **Lowest markets by revenue:** Saudi Arabia, Bahrain, Czech Republic
- European countries consistently outperformed other regions; Asian markets showed significantly lower revenue levels

### 3. Top Customers by Revenue

- The highest-spending customer generated **£280,206.02** in total revenue
- Customer ranking highlights a significant gap between top and low-spending customers, useful for targeting loyalty or re-engagement strategies

### 4. Global Product Demand

- Demand patterns align closely with revenue rankings — Netherlands, Eire, and Germany also lead on quantity sold
- Saudi Arabia, Bahrain, and RSA recorded the lowest product demand, consistent with their revenue positions

---

## Key Takeaways

- Revenue is highly seasonal — Q4 peaks and early-year dips suggest the business is heavily influenced by holiday shopping cycles
- European markets are the strongest international opportunity outside the UK
- A small number of high-value customers drive a disproportionate share of revenue — a strong case for customer retention strategies

---

## Recommendations

1. **Plan inventory and marketing around Q4** — September through November is the highest-growth window
2. **Investigate December drop-off** — explore whether post-holiday decline can be mitigated with January promotions
3. **Prioritise top international markets** — Netherlands, Eire, and Germany present the strongest growth opportunity outside the UK
4. **Re-engage low-spending customers** — identify customers with minimal purchases and design targeted campaigns to increase lifetime value

---
