# Vendor Performance & Retail Profitability Analytics

## Overview

This project evaluates vendor performance and retail inventory dynamics to drive strategic insights for purchasing, pricing, and inventory optimization. A complete data pipeline was built using SQL for ETL, Python for analysis and hypothesis testing, and Power BI for visualization.

---

## Table of Contents

- [Overview](#overview)
- [Business Problem](#business-problem)
- [Dataset](#dataset)
- [Tools & Technologies](#tools--technologies)
- [Data Cleaning & Preparation](#data-cleaning--preparation)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Research Questions & Key Findings](#research-questions--key-findings)
- [Power BI Dashboard](#power-bi-dashboard)
- [Project Workflow](#project-workflow)

---

## Business Problem

Retail businesses often struggle to:

- Identify underperforming brands needing pricing or promotional adjustments
- Understand which vendors truly contribute to profits
- Decide whether bulk purchasing reduces cost effectively
- Detect inventory turnover inefficiencies and dead stock
- Validate vendor profitability differences using statistical evidence

---

## Dataset

- Multiple CSV files located in /data/ folder (sales, vendors, inventory)
- Summary table created from ingested data and used for analysis
- These were integrated into a summary analytical table for further analysis.

---

## Tools & Technologies

| Tool | Purpose |
|------|---------|
| SQL | ETL, joins, CTEs, summary table creation |
| Python (Pandas, Matplotlib, Seaborn, SciPy) | EDA, visualization, hypothesis testing |
| Power BI | Interactive dashboards |
| GitHub | Version control and documentation |

---

## Data Cleaning & Preparation

- Removed transactions where:
  - Gross Profit ≤ 0
  - Profit Margin ≤ 0
  - Sales Quantity = 0
- Corrected data types and handled outliers
- Merged lookup tables
- Created vendor-level summary metrics

---

## Exploratory Data Analysis (EDA)

### Data Issues Identified

| Issue | Observation | Business Impact |
|------|-------------|-----------------|
| Negative Gross Profit | Min: -52,002.78 | Loss-making transactions |
| Infinite Profit Margins | Invalid cost values | Data inconsistency |
| Unsold Inventory | High stock value | Slow-moving items |

### Correlation Insights

| Variables | Correlation | Insight |
|-----------|-------------|--------|
| Purchase Qty vs Sales Qty | **0.999** | Overstocking pattern |
| Purchase Price vs Profit | Weak | Price alone doesn’t drive profit |
| Sales Price vs Profit Margin | -0.179 | Higher price does not ensure higher margin |

---

## Research Questions & Key Findings

### Brands Needing Promotion
- 198 brands with low sales but high profit margins
- Ideal for marketing and promotional focus

### Vendor Dependency Risk
- Top 10 vendors contribute 65.69% of total purchases
- Indicates over-reliance on limited vendors

### Bulk Purchasing Benefit
- 72% reduction in per-unit cost in large orders

### Inventory Turnover Issue
- $2.71M worth of unsold inventory detected

### Vendor Profitability Comparison

| Vendor Category | Mean Profit Margin |
|------------------|-------------------|
| High-performing Vendors | 31.17% |
| Low-performing Vendors | 41.55% |

Lower-volume vendors were observed to have higher margins.

### Hypothesis Testing

Statistical testing confirmed a significant difference in profit margins between vendor groups, indicating different pricing and supply strategies.

---

## Power BI Dashboard

The dashboard visualizes:

- Vendor-wise sales and profit margins
- Inventory turnover analysis
- Bulk purchase savings
- Performance heatmaps
- KPI-driven business insights

---

## Project Workflow

1. Data ingestion from CSV files  
2. SQL-based ETL and summary table creation  
3. Python-based EDA and statistical testing  
4. Visualization and reporting in Power BI  
5. Documentation and version control in GitHub  
