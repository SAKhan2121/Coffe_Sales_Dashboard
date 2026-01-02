#Coffee Sales Dashboard – Excel Project
📌 Project Overview
This project showcases an end‑to‑end Excel workflow to build a dynamic, interactive Coffee Sales Dashboard from raw transactional data.

1️⃣ Data Sources
Orders Table
Fields: Order ID, Order Date, Customer ID, Product ID, Quantity Customers Table,
 Customer ID, Name, Email, Country, City, Loyalty Card Status Products Table,
 Product ID, Coffee Type, Roast Type, Size, Unit Price, Profit.

2️⃣ Data Preparation & Cleaning
Remove duplicate records from all tables.
Standardize date formats and text fields (country, coffee type, roast).
Convert data ranges to Excel Tables for dynamic ranges.
Create a clean Orders master table that will feed all analyses.

3️⃣ Data Enrichment (Lookups)
Use XLOOKUP to bring customer details (Name, Email, Country, Loyalty) into the Orders table.
Use a dynamic INDEX–MATCH–MATCH setup to pull product details (Coffee Type, Roast, Size, Unit Price).
Lock ranges with absolute references to allow safe autofill.

4️⃣ Calculated Columns
Create Sales = Unit Price × Quantity.
Convert coffee and roast codes to full names using nested IF (or IFS) formulas.
Apply custom number formats for dates (dd-mmm-yyyy), sizes (e.g., 1.0 kilo), and currency (USD).

5️⃣ Pivot Tables & Pivot Charts
Build a pivot for Total Sales Over Time by Coffee Type and convert to a line chart.
Build a pivot for Sales by Country and convert to a bar chart.
Build a pivot for Top 5 Customers using value filters and convert to a bar chart.
Format all charts (colors, labels, axis titles) to match the dashboard theme.

6️⃣ Interactivity (Timeline & Slicers)
Insert a Timeline on Order Date to filter by year/month.
Insert Slicers for Roast Type, Package Size, and Loyalty Card Status.
Use Report Connections to connect the timeline and all slicers to every pivot table.
Test that changing any filter updates all charts simultaneously.

7️⃣ Dashboard Layout & UX
Create a dedicated Dashboard worksheet.
Add a title banner and place all charts, slicers, and timeline in a clean layout.
Align visuals to cell grid for a neat structure.
Hide gridlines, formula bar, headings, and (optionally) scroll bars for a focused view.

8️⃣ Files in This Repository
Coffee_Dashboard.xlsx – Final interactive dashboard.
Raw_Data.xlsx or /data/ – Source Orders, Customers, Products tables.
README.md – Project description and build steps (this file).

9️⃣ How to Use
Download and open the Excel file.
Go to the Dashboard sheet.
Use the timeline and slicers to filter by date, roast type, size, and loyalty status.
Explore how sales trends, countries, and top customers change with each filter.
