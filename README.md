Objective

To analyze e-commerce customer behavior and sales performance by tracking user interactions such as product views, cart additions, removals, and purchases using Power BI.
The dashboard focuses on understanding conversion funnels, cart abandonment patterns, revenue trends, and product performance to support data-driven decision-making in online retail environments.

Dataset

E-Commerce Behavior Dataset (Kaggle)

The dataset contains real-world transactional and session-level data collected from a multi-category e-commerce platform.

Key Attributes:

Event Time (Timestamp of user action)

Event Type (view, cart, remove_from_cart, purchase)

Product ID

Category ID

Category Code

Brand

Price

User ID

User Session

Why this dataset?

Represents real-world e-commerce customer interaction data

Captures the complete shopping journey from view to purchase

Enables cart behavior and conversion funnel analysis

Suitable for behavioral analytics, sales analysis, and KPI-based dashboards

Well-aligned with business intelligence and retail analytics use cases

Process Followed (Step by Step)
1. Data Loading

The dataset was imported into Power BI Desktop using the Get Data (CSV) option.

Why?
To bring raw e-commerce transaction and event data into Power BI for transformation, modeling, and visualization.

2. Column Selection and Cleaning

Only relevant columns required for analytics and KPI calculation were retained.

Columns Kept:

event_time

event_type

product_id

category_code

brand

price

user_id

user_session

Data Cleaning Performed:

Removed the "UTC" text from event_time

Converted event_time to proper Date/Time format

Replaced missing category and brand values with "Unknown"

Why this selection?
The retained columns directly support cart behavior analysis, revenue calculations, and user session tracking.
Cleaning improves data quality and prevents calculation errors.

3. Helper Column Creation (Power Query)

Additional columns were created using Power Query:

Event Date (Date extracted from timestamp)

Event Hour (Hour of user activity)

Why?
These columns enable:

Time-based analysis

Daily and hourly behavior trends

Improved visualizations and filtering

4. Data Modeling

The dataset was maintained as a single fact table due to its event-driven structure.
Logical relationships were handled using DAX measures instead of multiple lookup tables.

Why?
This simplifies the model while maintaining flexibility for behavioral analytics and KPIs.

5. Master DAX Measures (KPIs)

The following DAX measures were created:

Total Events

Total Views

Add to Cart

Remove from Cart

Purchases

Total Revenue

Conversion Rate %

Cart Abandonment %

Why?
DAX measures allow dynamic calculations that respond to slicers, filters, and user interactions.

6. Conversion Funnel Analysis

A Funnel Chart was created using:

Total Views

Add to Cart

Purchases

Why?
The funnel visual clearly represents the customer journey and highlights conversion drop-offs and cart abandonment behavior.

7. Dashboard Layout Design

The dashboard was designed using a clean, structured layout with:

KPI cards at the top

Funnel and distribution visuals in the center

Trend and performance visuals at the bottom

Why?
This layout improves readability and helps users quickly identify key insights.

8. Visualizations

The following visuals were included in the dashboard:

KPI Cards for key metrics

Funnel chart for conversion analysis

Line charts for customer behavior and revenue trends

Bar and column charts for brand and category performance

Pie and donut charts for event type distribution

Treemap for revenue contribution by category and brand

Gauge chart for conversion rate performance

Table visual with conditional formatting for product performance

Slicers for date, category, and brand filtering

Why?
Multiple visualization types highlight different behavioral and sales patterns, supporting deeper insights.

9. Behavioral Analytics & Sales Insights

The dashboard enables analysis of:

Cart abandonment patterns

Customer interaction flow

Peak activity hours

Top-performing products and categories

Revenue contribution by brand

Why?
Behavioral analytics help businesses optimize pricing, promotions, and inventory planning.

10. Final Formatting and Optimization

Dark theme applied for professional appearance

Consistent color coding (Views – Blue, Cart – Orange, Purchase – Green)

Aligned visuals using gridlines

Clear titles and labels

Reduced visual clutter

Why?
Professional formatting improves dashboard usability, clarity, and presentation quality.

Final Outcome

The dashboard provides:

Clear visibility into customer shopping behavior

Identification of conversion bottlenecks and cart abandonment

Sales and revenue trend analysis

Product, brand, and category performance insights

Actionable KPIs for e-commerce optimization

Tools Used

Microsoft Power BI Desktop

Power Query Editor

DAX (Data Analysis Expressions)

Kaggle E-Commerce Dataset (CSV)

Conclusion

This project demonstrates how business intelligence tools like Power BI can transform raw e-commerce interaction data into meaningful insights.
By analyzing cart behavior, conversion funnels, and sales performance, the dashboard supports informed decision-making and helps improve online retail efficiency and profitability.