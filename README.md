# BIGW Sales Dashboard (Excel)

An interactive Excel dashboard analysing BIGW retail sales across **stores and e-retail** in Australia, from January 2024 to December 2025. It turns 4,505 transaction records into a one-page view of sales trends, geography, categories, managers and buyers.

![BIGW Excel Dashboard](Big_w_excel_dashboard.png)

## Key Figures

| Metric | Value |
|---|---|
| Total sales | **$1,853,423** |
| Average sale (per transaction) | **$411.41** |
| Top suburb | **Frankston** ($32,011) |
| Top manager | **Jarrah Walker** ($148,593) |
| Top buyer | **Adelaide Scott** ($317,263) |

## Key Insights

- **Stores drive most of the sales.** BIGW Store makes up 72% ($1,328,396) of sales versus 28% ($525,027) for E-Retail.
- **NSW leads the states**, with $556,315 (about 30% of total sales), followed by Victoria ($445,822) and Queensland ($396,008).
- **Gaming, Tech & Audio is the top category** ($317,263). School, Office & Art Supplies is the smallest ($52,926).
- **Manager rankings are very close at the top.** Jarrah Walker ($148,593) and Arjun Sharma ($148,583) are separated by only $10.
- **Sales are broadly stable month to month**, with the average transaction sitting around $400 across the whole period.

## Dashboard Features

- **KPI cards:** Total Sales, Average Sales, Top Suburb, Top Manager, Top Buyer.
- **Type slicer:** filter the whole dashboard by BIGW E-Retail or BIGW Store.
- **Charts:**
  - Total Sales Over Time (line)
  - Average Sales Over Time (area)
  - Sales by Suburb, Top 10 (column)
  - Sales by Manager, Top 10 (column)
  - Online vs Store Sales (pie)
  - Sales by Category (bar)
  - Sales by State (map)
  - Sales by Buyer (100% stacked bar)
- **Colour coding:** blue = BIGW Retail (e-retail), green = BIGW Store, used consistently across the charts.

## Dataset

**Sheet:** `BIGW DATA` (Excel table `Data3`), 4,505 rows and 13 columns, with no missing values or duplicate rows.

| Column | Description |
|---|---|
| Date | Transaction date (6 Jan 2024 to 31 Dec 2025) |
| Financial Year / Financial Year2 | Australian financial year (e.g. 2024-2025) |
| Type | `BIGW STORE` or `BIGW E-RETAIL` |
| Suburb, Full State, State, Postcode, Country | Location of the sale (97 suburbs, 8 states/territories) |
| Manager | Managing person (21 managers) |
| Category | Product category (10 categories) |
| Buyer | Buyer responsible for the category (10 buyers) |
| Sales | Sales value in AUD |

## Workbook Structure

| Sheet | Purpose |
|---|---|
| **Main Dashboard** | The final one-page dashboard with KPIs, slicer and all charts |
| **BIGW DATA** | Source data table |
| Total Sales Over Time | Pivot + chart for monthly sales |
| Average Sales Over Time | Pivot + chart for average sale by month |
| Sales by Suburb | Top 10 suburbs |
| Sales by Manager | Top 10 managers |
| Sales by Category | Sales by product category |
| Sales by buyer | Sales by buyer |
| Online VS Store Sales | Channel split |
| Map-Sales by State / Total Sales and Trends by State | State totals for the map and monthly state trends |

## How It Was Built

1. Cleaned and structured the raw data as an Excel Table (`Data3`), adding Financial Year fields.
2. Built **PivotTables** for each view (time, suburb, manager, category, buyer, state, channel).
3. Created a chart from each pivot and applied a consistent colour scheme.
4. Added **KPI cards** and a **slicer** on `Type`, connected to the pivots for interactive filtering.
5. Arranged everything on the **Main Dashboard** sheet.

**Tools:** Microsoft Excel (PivotTables, PivotCharts, Slicers, Map chart).

## How to Use

1. Download `BigW - Sales Dashboard - Data.xlsx` and open it in Microsoft Excel (desktop version recommended, because the map chart and slicers need it).
2. Go to the **Main Dashboard** sheet.
3. Click **BIGW E-RETAIL** or **BIGW STORE** in the **Type** slicer to filter the charts. Use the clear-filter icon to reset.
4. To refresh after editing the data, go to **Data → Refresh All**.

## Notes and Limitations

- **Partial financial years.** The data starts in January 2024 and ends in December 2025, so FY2023-24 covers only Jan–Jun 2024 and FY2025-26 covers only Jul–Dec 2025. Only FY2024-25 is a full year, so compare years with care.
- **Buyers map one-to-one to categories** (for example, Adelaide Scott covers only Gaming, Tech & Audio), so the Buyer and Category charts show the same information.
- **Slicer state.** The dashboard's KPI cards show totals for all types. Check that the slicer is cleared before reading them as overall numbers.
- The map chart uses Bing maps, so it needs an internet connection to render.

## Repository Contents

```
├── BigW - Sales Dashboard - Data.xlsx   # Workbook with data, pivots and dashboard
├── Big_w_excel_dashboard.png            # Dashboard screenshot
└── README.md
```

## Author

**Yukta Chavan**, Data Analyst
[LinkedIn](https://www.linkedin.com/) · [GitHub](https://github.com/chavanyukta) · chavanyukta@gmail.com
