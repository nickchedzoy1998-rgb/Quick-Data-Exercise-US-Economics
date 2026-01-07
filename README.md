# Economic-Analysis
Small data analysis project using the FRED API to examine US unemployment trends across states, including data ingestion, cleaning, and visualisation in Python.

## Overview

This project explores **US unemployment trends at both national and state level** using data from the **Federal Reserve Economic Data (FRED)** API.
The goal is to demonstrate **handful of data analysis skills**: API ingestion, data cleaning, transformation, and exploratory visualisation using Python.

The analysis focuses on:

* Long-run unemployment trends
* State-level variation
* The impact of major macro events (e.g. COVID-19 shock)
---
## Data Source

* **Federal Reserve Economic Data (FRED)**

  * National unemployment rate (`UNRATE`)
  * Monthly, seasonally adjusted **state unemployment rates**
  * Units: percentage

Accessed programmatically via the `fredapi` Python package.

---

## Key Questions Explored

* How has US unemployment evolved over time?
* How large are differences in unemployment rates across states?
* Which states were most affected during the 2020 COVID shock?
* How do state-level trends compare to the national average?

---

## Methodology

1. **API Access**

   * Secure FRED API key loaded via environment variables
   * Automated series discovery using FRED search functionality

2. **Data Cleaning & Structuring**

   * Filtered to:

     * Monthly frequency
     * Seasonally adjusted series
     * Percentage units
   * Standardised state naming
   * Constructed a unified state-by-date dataframe

3. **Exploratory Analysis**

   * National unemployment time series
   * Cross-sectional state comparisons
   * Event-specific snapshots (e.g. May 2020)
   * Ranking and distribution analysis

4. **Visualisation**

   * Matplotlib for static charts
   * Consistent styling and readable formatting
   * Focus on clarity over decoration

---

## Key Insights

* National unemployment displays clear cyclical behaviour aligned with recessions.
* State-level unemployment dispersion increases sharply during economic shocks.
* COVID-19 caused unprecedented short-term divergence across states, with service-heavy economies hit hardest.
* Post-2020 recovery paths differ meaningfully by state, highlighting structural differences.

---

## Tools & Libraries

* Python
* `pandas`, `numpy`
* `matplotlib`
* `plotly`
* `fredapi`
