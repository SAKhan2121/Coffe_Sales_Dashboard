# Coffee Sales Dashboard — Excel Project Analysis
Hello, Everyone! ☕

I'm excited to share my latest project in the Data Analytics & Business Intelligence domain, focused on Building an Interactive Coffee Sales Dashboard using advanced Excel techniques for data-driven decision-making.

##🎯 Project Context
Scenario: Coffee retail company with multi-country operations (US, Ireland, UK)
Challenge: Disconnected sales data across Orders, Customers, and Products tables with no unified view
Goal: Enable leadership to explore sales trends, customer behavior, and product performance through a single interactive dashboard
Scope: Consolidate 3+ data sources, transform raw data, and build self-service BI analytics

#🎪 Objective
Build an interactive Power BI-style dashboard in Excel for real-time sales exploration
Identify high-performing coffee types and customer segments for targeted strategy
Align product portfolio (roast types, package sizes) with customer demand patterns
Enable data-driven decisions on product mix and regional marketing focus

#🛠️ Tools Used
 Excel | Data Transformation | Pivot Tables & Charts

#📊 Dashboard Overview
1. Login Page / Navigation Hub
Central control dashboard with visual navigation
Quick access to all analytical modules
Executive summary metrics at a glance

2. Demographics Analysis Dashboard
Customer distribution by Age, Income, Occupation, Gender, and City
Segment identification: Premium, Mid-tier, Budget customers
Geographic heat-mapping of high-value customer concentrations

3. Financial Behavior Analysis Dashboard
Spending patterns by customer segment and roast type
Payment preferences (credit card dominance vs. UPI adoption)
Purchase frequency & seasonality trends
Category-wise spending breakdown (Bills, Groceries, Apparel, Entertainment).

4. Executive Dashboard
KPI Summary: Total Sales, Avg Order Value, Customer Count, Repeat Purchase Rate
Key metrics for decision-makers at a glance
Drill-down capability into supporting dashboards

5. Interactive Filtering System
Timeline Filter: Dynamic date range selection across all dashboards
Slicers: Roast Type, Package Size, Loyalty Card Status, Region
Report Connections: All filters synchronized across 4+ dashboards

#🔍 Insights & Recommendations

#🎯 Target Segment
Focus on customers aged 25-34 (~37%) and Emerging Affluent (₹40K–₹80K, ~68%) professionals
Highest credit card adoption and spending propensity
Strong response to premium product positioning
Optimal for credit card partnerships & exclusive loyalty programs

#💰 Spending Potential
~30% of customers spend >50% of their income — prime candidates for premium tier benefits
Tailor post-purchase upsell and financial products offers
High lifetime value segment if properly engaged

#🌍 City Trends
UK leads in volume & spend; USA lags — customize regional campaigns by city performance
High variation in regional preferences suggests localized product mix optimization
Opportunity: Run targeted city-specific promotions

#🛍️ Spending Categories Lead
Bills & Groceries dominate → Leverage for everyday spending narratives
Food, Apparel, Entertainment show secondary strength → Bundle offerings opportunity
Category insights inform co-branded partnerships and loyalty rewards

#💳 Payment Trends
Credit Cards dominate (41%), but UPI surge among <25-age group → bimodal customer base
Integrate credit card rewards with UPI-based platforms
Offer dual payment incentives to capture both segments

#📈 Growth Areas
Launch co-branded credit cards aligned with customer spending profiles (Coffee + Lifestyle)
Business credit cards for emerging entrepreneurs (high spending, category diversification)
Premium tier benefits: Exclusive coffee blends, priority delivery, lounge access
UPI integration: Digital-first younger customers need seamless payment experience

#📈 Data Processing & Dashboard Build Steps:

Step 1: Data Integration & Structuring
Consolidated 3 data sources: Orders, Customers, Products tables
Identified relationships: Primary keys (Customer ID, Product ID), foreign keys
Created normalized schema for scalable analytics

Step 2: Data Cleaning & Enrichment
XLOOKUP formula: Pulled Customer Name, Email, Country from Customers table into Orders
Formula: =IF(XLOOKUP(customer_id, [lookup_range], [return_range])=0, "", value)
Handled missing values with IF condition to replace errors with blanks
INDEX-MATCH (Double formula): Dynamic product lookup across multiple columns
First MATCH: Located row by Product ID
Second MATCH: Located column by header name (Coffee Type, Roast Type, Size)
Single formula dragged horizontally & vertically for scalability
Data Validation: Removed duplicates, verified referential integrity across tables

Step 3: Data Transformation
Coded-to-Readable conversion: Nested IF functions
Coffee Types: ROB→Robusta, EXE→Excelsa, ARA→Arabica, LIB→Liberica
Roast Types: D→Dark, L→Light, M→Medium
Loyalty Status: 1→Yes, 0→No
Calculated fields:
Sales = Unit Price × Quantity
Customer Lifetime Value = Sum of Sales by Customer
Segment = Income Bracket categorization.

Step 4: Data Formatting Best Practices
Date Format: Custom dd-mmm-yyyy (e.g., 05-Sep-2024) to eliminate US/EU ambiguity
Currency: Applied US$ format to all monetary values
Units: Custom formatting for package sizes: 0.0" kilo" → displays as "1.0 kilo"
Number Format: Added thousand separators for sales figures.

Step 5: Excel Table Conversion
Converted data range to named Excel Table ("Orders_Table")
#Benefits:
Automatic range expansion with new data
Pivot tables auto-refresh seamlessly
Structured references for cleaner formulas
Professional alternating row colors.

Step 6: Pivot Table Strategy & Creation
Pivot Table 1: Total Sales Over Time by Coffee Type
Rows: Order Date (grouped by Year, Quarter, Month)
columns: Coffee Type (Arabica, Excelsa, Liberica, Robusta)
Values: Sum of Sales
Chart: Line Chart for trend visualization
Styling: Custom purple background, white gridlines, color-coded lines per coffee type
Pivot Table 2: Sales by Country
Rows: Country (US, Ireland, UK)
Values: Sum of Sales (sorted ascending)
Chart: Horizontal Bar Chart
Styling: Individual color scheme (US: dark green, Ireland: medium, UK: light green)
Data Labels: USD values on bars for clarity
Pivot Table 3: Top 5 Customers by Revenue
Rows: Customer Name
Values: Sum of Sales (filtered to Top 5)
Chart: Bar Chart
Insight: Identify VIP customers for retention strategies.

Step 7: Interactive Filtering Layer
Timeline Control:
Filter by Order Date across all dashboards
Customized styling: Purple fill, white bold fonts, bright highlight for selected periods
Enables year/quarter/month-level analysis
Slicer Controls (4 Total):
Roast Type Slicer: Dark, Light, Medium (3-column layout)
Package Size Slicer: 0.2kg, 0.5kg, 1.0kg, 2.5kg (4-column layout)
Loyalty Card Status Slicer: Yes, No (2-column layout)
Region Slicer: US, Ireland, UK
Styling: Dark purple fill (RGB 60,20,100), white bold text, strikethrough for unavailable items.

Step 8: Report Connections & Synchronization
Critical Step: Connected all slicers and timelines across pivot tables
Process: Timeline/Slicer → Report Connections → Check all pivot tables
Result: Single filter updates all 4 dashboards simultaneously
Tested all combinations: roast type, size, loyalty card, date range.

Step 9: Dashboard Assembly & Layout
Created dedicated "Dashboard" worksheet
Title section: Purple-filled shape with white text ("Coffee Sales Dashboard")
Visual hierarchy: Line chart (top), bar charts (middle), filters (bottom)
Aligned elements by cell snapping for pixel-perfect consistency
Responsive layout adapts to screen sizes

Step 10: UX Polish & Professionalization
Hidden UI Elements:
Removed gridlines (View → Gridlines)
Hidden formula bar (Options → Advanced)
Hidden scroll bars & sheet tabs
Hidden row/column headers
Result: Clean, focused interface where only filters and analytics are visible.
