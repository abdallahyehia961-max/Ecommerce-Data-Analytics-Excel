# Superstore Power BI Analytics

An end-to-end **Power BI Business Intelligence project** built on the Superstore dataset to analyze sales, profitability, products, customers, regional performance, shipping, and returns.

The solution contains **6 interactive dashboards** designed to turn transactional data into clear business insights and support data-driven decision-making.

---

## 📊 Project Overview

This project covers the complete analytics workflow:

- Data exploration and business understanding
- Data cleaning and preparation
- Data modeling
- DAX measures and KPI development
- Interactive dashboard design
- Sales and profitability analysis
- Product and customer analysis
- Regional and manager performance analysis
- Shipping and returns analysis
- Business insights and recommendations

---

## 🔢 Key KPIs

| KPI | Value |
|---|---:|
| Total Revenue | **$2.297M** |
| Total Profit | **$286.397K** |
| Profit Margin | **12.47%** |
| Total Orders | **5.009K** |
| Total Quantity | **37.873K** |
| Total Customers | **793** |
| Total Products | **1.86K** |
| Returned Orders | **296** |
| Return Rate | **5.91%** |
| Average Delivery Days | **3.96** |

---

# 📈 Dashboards

## 1️⃣ Executive Overview

A high-level view of overall business performance.

- Total Revenue
- Total Profit
- Total Quantity
- Total Orders
- Average Revenue
- Revenue by Category
- Orders by Category
- Profit by City
- Monthly Profit Trend
- Revenue by Customer Segment

![Executive Overview](01_executive_overview.jpg)

---

## 2️⃣ Sales & Profitability

Focused on understanding sales quality, profitability, discounts, and loss-making activity.

- Revenue
- Profit
- Profit Margin
- Average Discount
- Loss-Making Sales
- Revenue & Profit by Sub-Category
- Discount vs Profit
- Profit Margin by Category
- Profit by Sub-Category
- Sales & Profit Trend

![Sales & Profitability](02_sales_profitability.jpg)

---

## 3️⃣ Product Performance

Evaluates which products and categories drive revenue and which products reduce profitability.

- Total Products
- Product Revenue
- Product Profit
- Product Profit Margin
- Top 10 Products by Revenue
- Bottom 10 Products by Profit
- Sales vs Profit by Product
- Category & Sub-Category Performance
- Product Revenue Pareto Analysis

![Product Performance](03_product_performance.jpg)

---

## 4️⃣ Customer Analysis

Analyzes customer value, profitability, segmentation, and contribution to business performance.

- Total Customers
- Revenue per Customer
- Profit per Customer
- Top 10 Customers by Revenue
- Top 10 Customers by Profit
- Revenue by Customer Segment
- Customer Revenue vs Profit

![Customer Analysis](04_customer_analysis.jpg)

---

## 5️⃣ Regional Performance

Compares sales and profitability across regions, states, and managers.

- Total States
- Revenue & Profit by Region
- Revenue by State
- Profit by State
- Revenue & Profit by Manager
- Geographic performance analysis

![Regional Performance](05_regional_performance.jpg)

---

## 6️⃣ Shipping & Returns

Analyzes delivery performance, shipping methods, and return behavior.

- Total Orders
- Returned Orders
- Return Rate
- Average Delivery Days
- Orders by Ship Mode
- Average Delivery Days by Ship Mode
- Return Rate by Region
- Return Rate by Ship Mode
- Returned Orders by Category
- Returned Orders by Sub-Category

![Shipping & Returns](06_shipping_returns.jpg)

---

# 💡 Key Business Insights

- The business generated approximately **$2.297M in revenue** and **$286.4K in profit**.
- Overall **Profit Margin is 12.47%**.
- The **Consumer** segment contributes the largest share of revenue.
- **Technology** is one of the strongest categories in both revenue and profitability.
- **Furniture** generates strong revenue but has a significantly weaker profit margin.
- Several products generate high revenue while producing weak or negative profit.
- **California** and **New York** are among the strongest states by profit.
- The **West region** shows the highest return rate at approximately **11.73%**.
- **Same Day** shipping has the highest return rate among ship modes at approximately **7.20%**.
- **Standard Class** is the most frequently used shipping method and has the longest average delivery time.
- Returned-order analysis highlights **Office Supplies**, especially **Binders** and **Paper**, as areas for further investigation.

---

# 🧮 DAX & Analytics Techniques

The project applies a range of DAX concepts, including:

- `SUM`
- `SUMX`
- `AVERAGE`
- `AVERAGEX`
- `DISTINCTCOUNT`
- `DIVIDE`
- `CALCULATE`
- `FILTER`
- `ALL`
- `RANKX`
- `TREATAS`
- `DATEDIFF`
- `VAR` / `RETURN`
- Ranking
- Pareto / cumulative analysis
- Profitability analysis
- Return-rate analysis

Full DAX documentation:

[📘 DAX Measures](DAX_MEASURES%20%281%29.md)

---

# 🗂️ Data Model

The Power BI model includes:

- `Orders`
- `Returns`
- `Mangers`
- `calender`
- `Calculation`

The Calendar table is used for time-based filtering and analysis, while the Orders table acts as the primary transaction table.

---

# 📁 Repository Structure

```text
Superstore-PowerBI-Analytics/
│
├── projectttt.pbix
├── README.md
├── DAX_MEASURES (1).md
├── Superstore_PowerBI_Project_Report.pdf
├── Superstore_PowerBI_Project_Report.docx
├── Superstore_PowerBI_Presentation.pptx
├── Superstore_PowerBI_Presentation.pdf
│
├── 01_executive_overview.jpg
├── 02_sales_profitability.jpg
├── 03_product_performance.jpg
├── 04_customer_analysis.jpg
├── 05_regional_performance.jpg
└── 06_shipping_returns.jpg
```

---

# ▶️ How to Open the Project

1. Install **Microsoft Power BI Desktop**.
2. Clone or download this repository.
3. Open:

```text
projectttt.pbix
```

4. Navigate through the six dashboard pages.
5. Use slicers and interactive visuals to explore the analysis.

---

# 📄 Project Documentation

The repository includes:

- [📄 Full Project Report - PDF](Superstore_PowerBI_Project_Report.pdf)
- [📝 Full Project Report - Word](Superstore_PowerBI_Project_Report.docx)
- [📊 Presentation - PowerPoint](Superstore_PowerBI_Presentation.pptx)
- [📑 Presentation - PDF](Superstore_PowerBI_Presentation.pdf)
- [🧮 DAX Measures](DAX_MEASURES%20%281%29.md)

---

# 🛠️ Tools & Skills

**Power BI | Power Query | DAX | Data Modeling | Data Visualization | Business Intelligence | KPI Design | Sales Analysis | Customer Analysis | Product Analysis | Geographic Analysis | Shipping & Returns Analysis**

---

## 👤 Author

**Abdallah Mohamed Yehia**

Data Analytics / Business Intelligence Project
