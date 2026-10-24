<div align="center">

# E-Commerce Analytics | Excel BI Portfolio

### From millions of raw records to four interactive, decision-focused dashboards

**Microsoft Excel · Power Query · Power Pivot · DAX · Data Modeling · Business Intelligence**

[![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=flat-square&logo=microsoftexcel&logoColor=white)](https://www.microsoft.com/microsoft-365/excel)
![Power Query](https://img.shields.io/badge/Power_Query-Data_Preparation-087E8B?style=flat-square)
![Power Pivot](https://img.shields.io/badge/Power_Pivot-Data_Modeling-2361A8?style=flat-square)
![DAX](https://img.shields.io/badge/DAX-Business_Measures-6844AD?style=flat-square)
![Dashboards](https://img.shields.io/badge/Dashboards-4_Interactive-0AA6A6?style=flat-square)

**125K+ orders · 100K customers · 2.43M+ website events · 4 dashboards**

</div>

---

## Project at a glance

I built this end-to-end **e-commerce analytics solution entirely in Microsoft Excel** to turn transactional, customer, product, inventory, and website activity data into a connected view of business performance.

The work goes beyond chart creation: it combines **data quality checks, relational modeling, reusable DAX measures, KPI definition, and dashboard design** to answer questions that matter to business teams.

> **My focus:** build an analytical model that explains *what is happening*, highlights *where to investigate*, and gives decision-makers a clear way to explore the data.

### Dashboard home page

![E-Commerce Analytics — Home Page](screenshots/00-home.png)

---

## Key performance indicators

*Model-level figures below represent the unfiltered analytical baseline. Some dashboard screenshots may show different values due to filters or the state of particular PivotTables.*

| Business metric | Result |
|:--|--:|
| **Completed Sales** | **$2,715,783.74** |
| **Gross Profit** | **$1,409,923.37** |
| **Gross Profit Margin** | **51.92%** |
| **Total Orders** | **125,226** |
| **Completed Orders** | **31,354** |
| **Completed Units** | **45,609** |
| **Total Customers** | **100,000** |
| **Customers With Orders** | **80,044** |
| **Repeat Customers** | **30,212** |
| **Repeat Customer Rate** | **37.74%** |
| **Products in Catalog** | **29,120** |
| **Website Events** | **2,431,963** |
| **Website Sessions** | **681,759** |
| **Session Purchase Rate** | **26.66%** |

---

## Four analytical dashboards

### 01 — Executive Overview
**The big picture: sales, profitability, order performance, and critical KPIs.**

![Executive Overview](screenshots/01-executive-overview.png)

- Completed sales, gross profit, customer and order metrics
- Sales performance over time
- Top-performing product categories
- Distribution of orders by status
- Interactive year-based exploration

### 02 — Sales & Products
**Understand which products generate revenue and how profit varies across categories.**

![Sales and Products](screenshots/02-sales-products.png)

- Monthly sales performance and historical trends
- Leading product categories and brands
- Top-selling products
- Sales versus gross-profit comparisons
- Product pricing and volume metrics

### 03 — Customers & Orders
**Explore customer segments, purchasing behavior, and geographic patterns.**

![Customers and Orders](screenshots/03-customers-orders.png)

- Customer age-group distribution and demographics
- Completed, cancelled, returned, shipped, and processing orders
- High-value customer analysis
- Repeat-customer KPIs
- Geographic sales breakdowns

### 04 — Web & Funnel Analysis
**Connect website activity to engagement and purchase-related behavior.**

![Web and Funnel Analysis](screenshots/04-web-analytics.png)

- Traffic-source performance
- Event types and activity volume
- Browser-level session and purchase-rate comparisons
- Cities with high site activity
- Traffic-source versus event-type analysis
- Session purchase-rate KPI

**Analytical note:** Purchase events, product views, and cart events are event counts. They should **not** be interpreted as a user-level step-by-step conversion funnel unless users or sessions are tracked consistently between stages.

---

## Technology stack

| Technology | How I used it |
|:--|:--|
| **Excel** | Dashboard layout, navigation, charts, KPI cards, reporting |
| **Power Query** | Importing, cleaning, transforming, and standardizing source data |
| **Power Pivot** | Building the Data Model and relationships |
| **DAX** | Financial, customer, inventory, order, and website measures |
| **PivotTables / PivotCharts** | Aggregation and interactive visual analysis |
| **Slicers** | Filtering compatible PivotTables across dashboard views |

---

## Data preparation & analytical workflow

1. **Data ingestion** — Brought together seven CSV-based source tables covering users, orders, products, order items, inventory, website events, and distribution centers.
2. **Data quality** — Reviewed missing values, standardized types, corrected identifiers, and separated date values from timestamps where required.
3. **Data modeling** — Linked core tables inside Power Pivot and added a dedicated `Calendar` table for date-based analysis.
4. **Measure development** — Created reusable DAX metrics instead of manually entering chart values.
5. **Business analysis** — Explored sales trends, margins, orders, repeat customers, inventory, product leaders, traffic, and sessions.
6. **Reporting** — Designed four navigable Excel dashboards with KPI cards, PivotCharts, and slicers.

### Dataset overview

| Source table | Rows | Main analytical role |
|:--|--:|:--|
| `users` | 100,000 | Customer attributes and demographics |
| `orders` | 125,226 | Orders, order dates, and status |
| `order_items` | 181,759 | Item-level completed sales |
| `products` | 29,120 | Catalog, categories, and brands |
| `inventory_items` | 490,705 | Item costs and inventory status |
| `events` | 2,431,963 | Visitor sessions and event activity |
| `distribution_centers` | 10 | Distribution center information |
| `Calendar` | Generated | Year/month filtering and time intelligence |

### Data Model relationships

```text
Calendar ────────> orders <──────── users ────────> events
                      |
                      v
                 order_items
                      |
                      v
                inventory_items
                      |
                      v
                   products
                      |
                      v
              distribution_centers
```

*Arrows above illustrate related tables, not SQL join direction or the precise cross-filter direction configured in Power Pivot.*

---

## Selected DAX calculations

### Completed Sales

```dax
Completed Sales :=
CALCULATE(
    SUM(order_items[sale_price]),
    order_items[status] = "Complete"
)
```

### Cost of Completed Sales

```dax
Completed Sales Cost :=
CALCULATE(
    SUMX(
        order_items,
        RELATED(inventory_items[cost])
    ),
    order_items[status] = "Complete"
)
```

### Gross Profit

```dax
Gross Profit :=
[Completed Sales] - [Completed Sales Cost]
```

### Average Order Value

```dax
Average Order Value :=
DIVIDE([Completed Sales], [Completed Orders], 0)
```

Other measures cover **order completion, cancellation and return rates, customer repeat activity, inventory sell-through, average selling price, YTD performance, and session purchase rate**.

---

## Observations & business relevance

- **Sales and profitability:** Approximately **$2.72M** in completed sales and **$1.41M** in gross profit provide a baseline for analyzing product and category contribution.
- **Customer behavior:** **80,044** customers have placed orders; **30,212** are classified as repeat customers, supporting retention-oriented analysis.
- **Inventory exposure:** **308,946** inventory units were unsold, representing approximately **$8.85M** in unsold inventory cost under the model's definitions.
- **Digital activity:** The dataset contains **2.43M+ events**, making it possible to compare acquisition sources, browsers, events, and purchase-related sessions.
- **Time-series caution:** **2024 is a partial period** in the source data. Comparisons against complete prior years should be interpreted carefully.

These are **descriptive insights**; differences between segments or channels do not, by themselves, establish causation.

---

## How to explore the project

1. Review the dashboard previews in this README.
2. Download the `.xlsx` workbook **if it has been uploaded to this repository**.
3. Open it in **Microsoft Excel desktop** with Data Model / Power Pivot support.
4. Navigate between dashboard sheets using the workbook's navigation.
5. Use slicers to filter charts and measures connected to compatible PivotTables.

> GitHub displays the screenshots; the interactive PivotCharts, DAX model, and slicers run **inside Excel**, not on this GitHub page. Some query refreshes may require access to the original local CSV paths.

---

## Repository layout

```text
Ecommerce-Data-Analytics-Excel/
├── readme.md
└── screenshots/
    ├── 00-home.png
    ├── 01-executive-overview.png
    ├── 02-sales-products.png
    ├── 03-customers-orders.png
    └── 04-web-analytics.png
```

*The Excel workbook can be added separately. Large source CSV files are not required just to display these README previews.*

**Image setup:** Keep the five image files inside the `screenshots` folder **in the repository root**, with the exact names above. Upload the individual images/folder contents, **not only a ZIP archive**. GitHub image paths are case-sensitive.

---

<div align="center">

### Built with an analyst's mindset — not just a dashboard designer's toolkit.

**Data Preparation → Data Modeling → DAX → Business KPIs → Interactive Analytics**

**Developed by [Abdallah Yehia](https://github.com/abdallahyehia961-max)**

</div>
