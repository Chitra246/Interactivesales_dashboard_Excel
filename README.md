# Interactive Sales Dashboard — Excel Project

## Overview

This Excel workbook contains an interactive sales dashboard built on three years of transactional sales data (2020–2022). It is designed to give a quick visual summary of business performance across months, quarters, product categories, and regions — all driven by PivotTables and calculated summaries in a dedicated sheet.

---


https://github.com/user-attachments/assets/8fca3d63-bb74-4b97-8a0a-262a5634e09d

## Workbook Structure

The file is organised into three sheets:

### 1. `DASHBOARD`
The main presentation layer. Contains charts, summary KPIs, and interactive elements (slicers/filters) that allow users to explore the data visually. This is the sheet intended for end-user consumption.

### 2. `CAlCULATIONS`
The engine behind the dashboard. Houses PivotTables that aggregate the raw data by:

- **Month** — order count, total sales amount, quantity sold, and 10% profit per month
- **Quarter** — total sales amount per quarter (Q1–Q4)
- **Category** — total sales amount and quantity sold per product category
- **Grand Totals** — 981 total orders, ₹9,843,042 total revenue, 4,279.8 total units, ₹984,304 total profit

### 3. `DATA`
The raw transactional dataset. Each row represents a single order line with the following columns:

| Column | Description |
|---|---|
| `Order id` | Unique order identifier |
| `Order Date` | Date of the order (stored as Excel serial date) |
| `Year` | Calendar year (2020, 2021, or 2022) |
| `Cust ID` | Customer identifier (e.g. NN001) |
| `Region` | Sales region — East, West, North, South |
| `Cust Name` | Customer name (anonymised as Name 1, Name 2, …) |
| `Category` | Product category |
| `Product` | Product name |
| `Price` | Unit price |
| `Qty` | Quantity ordered |
| `Amount` | Total line value (Price × Qty) |
| `Profit 10%` | Estimated profit at a 10% margin |

---

## Data Summary

| Metric | Value |
|---|---|
| Total Orders | 981 |
| Total Revenue | ₹9,843,042 |
| Total Units Sold | 4,279.8 |
| Total Profit (10%) | ₹984,304 |
| Date Range | 2020 – 2022 |

### Product Categories

| Category | Revenue |
|---|---|
| Mobiles | ₹2,175,180 |
| Electronics | ₹1,999,150 |
| Storage | ₹2,016,958 |
| Art | ₹1,974,370 |
| Computer | ₹1,677,384 |

### Quarterly Performance

| Quarter | Revenue |
|---|---|
| Q1 (Jan–Mar) | ₹2,414,032 |
| Q2 (Apr–Jun) | ₹2,368,180 |
| Q3 (Jul–Sep) | ₹3,095,380 |
| Q4 (Oct–Dec) | ₹1,965,450 |

### Products

The catalogue includes: Mouse, Monitor, Printer, Scanner, Keyboard, SSD 256 GB, HDD 256 GB

### Regions

East · West · North · South

---

## How to Use

1. Open the file in Microsoft Excel (2016 or later recommended for full slicer support).
2. Navigate to the **DASHBOARD** sheet to view charts and KPIs.
3. Use any slicers or filter controls on the dashboard to drill down by year, region, or category.
4. The **CAlCULATIONS** sheet updates automatically — do not manually edit its PivotTables.
5. To add new data, append rows to the **DATA** sheet and then refresh all PivotTables (`Data → Refresh All`).

---

## Notes & Known Issues

- Order dates in the `DATA` sheet are stored as Excel serial numbers. Ensure regional date settings are correct if dates display unexpectedly.
- Some order IDs appear more than once, indicating either multi-line orders or duplicate entries — review before any deduplication analysis.
- The `CAlCULATIONS` sheet name contains a capitalisation irregularity (`CAlCULATIONS`) — this is as-built and referenced by existing formulas; renaming it may break links.
- In a small number of 2022 rows, price values appear to be shuffled across products, which may affect category-level unit economics. Verify before using price data for margin analysis.

---

## File Information

| Property | Detail |
|---|---|
| Filename | `Interactive_Sales_Dashboard.xlsx` |
| Format | Excel Workbook (.xlsx) |
| Sheets | 3 (DASHBOARD, CAlCULATIONS, DATA) |
| Row Count (DATA) | ~1,000+ transactions |
| Years Covered | 2020, 2021, 2022 |
