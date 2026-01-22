# Vendor Performance Analysis – Retail Inventory & Sales

Analyzing vendor efficiency and retail profitability to support strategic purchasing and inventory decisions using SQL, Python, and Power BI.

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

## Overview

This project evaluates vendor performance and retail inventory dynamics to generate insights for purchasing, pricing, and inventory optimization.

A complete data analytics pipeline was built using:

- SQL for ETL and data modeling
- Python for EDA and hypothesis testing
- Power BI for interactive business visualization

---

## Business Problem

Retail businesses often face challenges in:

- Identifying underperforming brands requiring promotions
- Understanding which vendors contribute most to profits
- Evaluating the financial benefit of bulk purchasing
- Detecting inventory turnover inefficiencies and dead stock
- Statistically validating vendor profitability differences

---

## Dataset

Data sourced from multiple CSV files stored in the `/data/` folder:

- Sales data
- Vendor data
- Inventory data

These datasets were merged into a summary analytical table for analysis.

---

## Tools & Technologies

- SQL – ETL, joins, CTEs, summary tables
- Python – Pandas, Matplotlib, Seaborn, SciPy
- Power BI – Interactive dashboards and KPI visuals
- GitHub – Version control and documentation

---

## Data Cleaning & Preparation

- Removed transactions where:
  - Gross Profit ≤ 0
  - Profit Margin ≤ 0
  - Sales Quantity = 0
- Corrected data types and treated outliers
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
| Purchase Qty vs Sales Qty | 0.999 | Overstocking pattern |
| Purchase Price vs Profit | Weak | Price alone doesn’t drive profit |
| Sales Price vs Profit Margin | -0.179 | Higher price does not ensure higher margin |

---

## Research Questions & Key Findings

### Brands Needing Promotion
- 198 brands identified with low sales but high margins

### Vendor Dependency Risk
- Top 10 vendors contribute 65.69% of total purchases

### Bulk Purchasing Benefit
- 72% reduction in per-unit cost in large orders

### Inventory Turnover Issue
- $2.71M worth of unsold inventory

### Vendor Profitability Comparison

| Vendor Category | Mean Profit Margin |
|------------------|-------------------|
| High-volume Vendors | 31.17% |
| Low-volume Vendors | 41.55% |

### Hypothesis Testing

Statistical testing confirmed a significant difference in profit margins between vendor groups, indicating different pricing strategies.

---

## Power BI Dashboard

The dashboard includes:

- Vendor-wise sales and profit margins
- Inventory turnover visualization
- Bulk purchase savings
- Performance heatmaps
- KPI-based decision support

---

## Project Workflow

1. Data ingestion from CSV files  
2. SQL ETL and summary table creation  
3. Python EDA and statistical testing  
4. Power BI dashboard creation  
5. Documentation on GitHub
