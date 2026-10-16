# business-intelligence-dashboard
An interactive business intelligence dashboard built in Microsoft Excel using Power Pivot, relational data models, DAX measures, and dynamic cross-filtering slicers.

# Excel Business Dashboard & Relational Data Model

An interactive, end-to-end business intelligence dashboard built in Microsoft Excel. This project demonstrates advanced data modeling, Power Pivot relationship management, DAX measures, and dynamic report visualization using relational sales data.

---

## Project Overview
This project transforms raw transactional data into actionable business insights. It simulates a complete retail analytics pipeline—starting from normalized relational tables to an interactive executive dashboard featuring dynamic KPI cards, PivotCharts, and cross-filtering slicers.

---

## Data Architecture & Relational Schema
The database consists of four interconnected tables linked by primary and foreign keys in the **Excel Data Model**:
* **`Sales_Data`** (Fact Table): Contains 20 transactional order records, including order IDs, dates, quantities, and sales amounts.
* **`Customers`** (Dimension Table): Customer demographics categorized by ID, name, and region.
* **`Products`** (Dimension Table): Product catalog detailing product IDs, names, categories, and unit costs.
* **`Stores`** (Dimension Table): Store locations categorized by store ID, store name, and city.

---

## Key Technical Features

### 1. Power Pivot & Data Modeling
* Established a relational star-schema by linking foreign keys from the `Sales_Data` table to the `Customers`, `Products`, and `Stores` dimension tables in Power Pivot diagram view.

### 2. DAX Measures Implemented
Calculated metrics built using Data Analysis Expressions (DAX):
* **Total Sales:** `SUM(sales_data[Sales Amount])`
* **Total Cost:** `SUMX(sales_data, sales_data[Quantity] * RELATED(Products[Unit Cost]))`
* **Total Profit:** `[Total Sales] - [Total Cost]`
* **Profit Percentage:** `DIVIDE([Total Profit], [Total Sales], 0)`

### 3. Interactive Dashboard & Visualizations
* **Helper PivotTables:** Structured summary blocks aggregating performance metrics by product category and geographic region.
* **GETPIVOTDATA Integration:** Dynamic cell linking ensuring robust data retrieval across custom dashboard layouts.
* **Executive KPI Cards:** Custom-styled shape cards displaying core financial performance metrics.
* **Interactive Slicers:** Region and Category slicers connected via **Report Connections** to enable simultaneous, cross-table filtering across all dashboard charts and metrics.


---
*Created by **Arnab Saha***
