##  Mobile Sales Performance Dashboard

This repository contains the source files and documentation for a comprehensive Power BI dashboard used to track and analyze **Mobile Sales Performance**.

The live, interactive dashboard can be viewed here:
➡️ **[https://app.powerbi.com/view?r=eyJrIjoiOWQ4OGI4NDEtZmI0NC00Yjc5LTg1MDgtYTI0N2ZlZDg5NjA0IiwidCI6IjEzMjc0YTYzLTYzNDEtNDQ3Yi1iNTM0LTdkNzRhYWM2MTc5MSJ9]**

-----

### 🎯 Project Goal

The project was designed to:

1.  **Consolidate** sales data from four disparate monthly Excel files.
2.  **Develop key performance indicators (KPIs)** and detailed visualizations to identify trends and regional performance.
3.  Provide a tool for analyzing **time-series trends** and **geographical sales distribution**.

### 📊 Key Features and Metrics

The dashboard provides deep insights via the following:

| Metric (DAX) | Value (From Dashboard) | Insight Highlighted |
| :--- | :--- | :--- |
| **Total Revenue** | **769 Million** | Overall sales achievement. |
| **Total Quantity Sold** | **19 Thousand** | Total volume of units sold. |
| **Total Orders/Transactions** | **40 Thousand** | Number of distinct sales events. |
| **Average Deal Size** | *$19,225* | Sales efficiency measure. |

**Key Visual Insights:**

  * **Geospatial Analysis:** A map visualization shows sales concentration in major Indian cities like Delhi, Mumbai, and Bangalore.
  * **Time Series Trend:** A line chart tracks **Total Quantity by Month** (Jan-Dec) for trend analysis.
  * **Payment Breakdown:** A pie chart illustrates the distribution of transactions across payment methods (e.g., UPI, Debit/Credit Card, Cash).
  * **Brand Performance:** A table and charts showcase top brands (**Apple, OnePlus, Samsung**) by sales volume and transaction count.

### 🛠️ Technical Implementation

#### 1\. Data Sources

The report utilized four separate Excel files, representing monthly sales data, located in the `/data` folder of this repository.

#### 2\. Data Transformation (Power Query M)

  * **File Consolidation:** Used Power Query's 'Combine Binaries' feature to successfully merge the four monthly Excel sheets into one unified fact table.
  * **Data Cleansing:** **Used Power Query to consolidate and append four separate monthly Excel files, followed by ensuring consistent City and Brand naming conventions.**

#### 3\. Data Modeling (Relationships & DAX)

  * **Data Model:** Implemented a robust **Star Schema** with a central sales fact table.
  * **Time Intelligence:** A dedicated **Calendar/Date Table** was created and linked to the fact table to enable accurate time intelligence (MoM analysis and dynamic monthly filtering).
  * **Key Measures:** Measures were defined for the primary KPIs, including time-intelligence functions for comparisons and aggregation.

### 📂 Repository Structure

```
├── data/
│   ├── January_23.xlsx
│   ├── February_23.xlsx
│   ├── March_23.xlsx
│   └── April_23.xlsx
├── Mobile Sales Dashboard.pbix  <-- The complete Power BI Desktop source file
└── README.md                   <-- You are here!
```

### ⚙️ How to Use

1.  Clone or download this repository.
2.  Ensure you have **Power BI Desktop** installed.
3.  Open the `Mobile Sales Dashboard.pbix` file. The report should connect and refresh the data from the local `data/` folder automatically.
