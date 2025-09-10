# Causal Impact Analysis of a Sales Promotion

This R project analyzes the causal impact of a simulated "free shipping" promotion on e-commerce sales, using the public Olist dataset from Brazil. The goal is to provide a data-driven estimate of the promotion's effectiveness and offer actionable business insights.

---

## Key Findings

* **Overall Effect**: The promotion caused a **statistically significant 19.7% average increase** in daily sales revenue.
* **Segmented Effect**: The impact was not uniform across product categories. The promotion was highly effective for `health_beauty` (+87%) and `bed_bath_table` (+75%), but was ineffective for categories like `cool_stuff` (-18.6%).
* **Robustness**: A placebo test was conducted which found a smaller but still significant effect on a fake intervention date. This suggests the main finding is strong, but other seasonal factors may also be influencing sales, indicating an area for future work.

---

## Methodology

The core of the analysis is a **Difference-in-Differences (DiD)** model, implemented as a **Two-Way Fixed Effects (TWFE)** regression using the `fixest` R package. This quasi-experimental method isolates the causal effect of the promotion by controlling for time-invariant state-specific trends and common shocks that affect all states over time.

## Project Structure

* `report.Rmd`: The fully documented and reproducible R Markdown notebook containing all code for data preparation, analysis, and visualization.
* `report.html`: The final, polished HTML report with all findings, plots, and tables.
* `data/`: Folder containing the raw CSV files used in the analysis.
