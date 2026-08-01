  # Sales-detailed-Analysis-POWER-BI-Dashboard-
Executive Sales Analytics Dashboard built with Power BI, DAX, and ML insights.
┌────────────────┐     ┌──────────────────┐     ┌──────────────────────┐     ┌──────────────────────┐
│  1. Data ETL   │ ──> │  2. DAX Measures │ ──> │ 3. Interactive Dash  │ ──> │ 4. Predictive Insights│
│ Power Query    │     │ Star Schema      │     │ 3-Page Power BI      │     │ ML Churn & RFM       │
└────────────────┘     └──────────────────┘     └──────────────────────┘     └──────────────────────┘


---

## 📊 Dashboard Structure & Visualizations

🟢 Page 1: Exploratory Data Analysis (EDA)
* **Header KPI Cards:** Total Orders (9,994), Sales ($2.30M), Profit ($286.4K), Avg Discount (15.5%).
* **Category Breakdown:** Stacked bar chart highlighting Technology ($836K Sales, $145K Profit) vs. Furniture ($742K Sales, $18K Profit).
* **Regional Distribution:** Donut chart showing West (31.6%), East (29.5%), Central (21.8%), and South (17.1%).
* **Logistics Analysis:** Treemap illustrating Standard Class shipping dominance (~59% of orders).

🔵 Page 2: Comparative Trends & Discount Sensitivity
* **Monthly Revenue & Seasonality:** Area chart highlighting recurring Q4 peak sales (Sept–Dec).
* **YoY Performance Comparison:** Line & Clustered Column chart tracking current vs. last year sales volume.


🟣 Page 3: Predictive Trends & Advanced Analytics
* **Sales Forecasting:** Native 10-month continuous forecast with 95% confidence interval.
* **AI Key Influencers:** Automated root cause analysis for profit drops and extreme outlier discounts.


## 📐 Key DAX Calculations

```dax
// Total Sales
Total Sales = SUM('Orders'[Sales])

// Total Profit
Total Profit = SUM('Orders'[Profit])

// Profit Margin %
Margin % = DIVIDE([Total Profit], [Total Sales], 0)

// Last Year Sales (Time Intelligence)
Last Year Sales = CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Calendar'[Date]))

// Year-over-Year Growth
YoY Sales Growth % = DIVIDE([Total Sales] - [Last Year Sales], [Last Year Sales], 0)
💡 Strategic Business Recommendations
Discount Caps: Enforce strict 15% discount caps on Furniture (Tables & Bookcases) to eliminate net losses.

Q4 Inventory Preparation: Align supply chain and warehouse stocking by August 15th to capture the recurring 35% seasonal spike.

High-Margin Bundling: Focus marketing campaigns on Technology products (Copiers, Phones) with ~17.4% margins.

Territory Optimization: Reallocate promotional budget from Central region to high-yield West & East territories.

👤 Author
Rameshwar Tawle
Role: Business Analyst (Operations & Systems)

Tools: Power BI | DAX 


with open("README.md", "w", encoding="utf-8") as f:
f.write(readme_content)
