# Causal Impact Analysis of a Sales Promotion

This R project analyzes the causal impact of a simulated "free shipping" promotion on e-commerce sales, using the public Olist dataset from Brazil. The goal is to provide a data-driven estimate of the promotion's effectiveness and offer actionable business insights.

---

## 📊 Key Results

### 1. Sales Trends Before & After Promotion

![Sales Trends Plot](outputs/sales_trends.png)
*Dashed line = promotion start. The plot shows that the sales trend for the treatment state (SP) diverges upwards from the control states after the promotion, supporting the core assumption of our model.*

### 2. Category-Level Promotion Effects

![Category Effects Plot](outputs/promotion_effects.png)
*The promotion was not uniformly effective. The bar chart clearly shows a strong, statistically significant lift for categories like `health_beauty`, while others like `cool_stuff` saw a negative effect.*

---

## 🔧 Methods & Tools
* **Data Wrangling**: `tidyverse`, `lubridate`
* **Modeling**: Two-Way Fixed Effects Regression (`fixest::feols`)
* **Validation**: Placebo Test for Robustness
* **Visualization**: `ggplot2`
* **Reporting**: R Markdown

## 🎓 Learning Reflection 

This project helped me practice:
* Joining and cleaning multiple relational datasets, with a focus on data quality assurance.
* Applying causal inference methods (Difference-in-Differences, Placebo Test).
* Translating complex regression results into business-ready insights and visualizations.

I also recognized key limitations (seasonality, model assumptions) and proposed improvements (A/B testing). I look forward to developing these skills further during the Google Data Analytics Apprenticeship.
