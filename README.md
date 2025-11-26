#🍕 Pizza Hut Sales Analysis – Power BI Dashboard

A Power BI dashboard built using Pizza Hut sales data to analyze revenue, orders, product performance, and customer buying patterns.
The report uses structured DAX calculations to provide insights into category trends, size contribution, monthly and daily behaviour, and top-selling pizzas.

#📌 Project Summary

This dashboard helps answer key business questions like:

Which pizza categories and sizes perform the best?

What are the peak order days and months?

Which pizzas are top sellers and which underperform?

What percentage of sales each category/size contributes?

How do customers generally behave in terms of order size and value?

The report is clean, interactive, and optimized for quick analysis.

#🧠 DAX Formulas Used
🔷 Core KPI Measures
Total Revenue = SUM(Sales[total_price])
Total Orders = DISTINCTCOUNT(Sales[order_id])
Total Pizzas Sold = SUM(Sales[quantity])
Avg Order Value = DIVIDE([Total Revenue], [Total Orders])
Avg Pizza Per Order = DIVIDE([Total Pizzas Sold], [Total Orders])

🔷 Category & Size Measures
Revenue by Category = SUM(Sales[total_price])
Quantity by Category = SUM(Sales[quantity])
Revenue by Size = SUM(Sales[total_price])
Quantity by Size = SUM(Sales[quantity])

🔷 Date Intelligence
Day Name = FORMAT(Sales[order_date], "DDD")
Month Name = FORMAT(Sales[order_date], "MMM")
Month Number = MONTH(Sales[order_date])

🔷 Pizza-Level Performance
Revenue by Pizza = SUM(Sales[total_price])
Quantity by Pizza = SUM(Sales[quantity])

🔷 % Contribution Metrics
% Category Sales = DIVIDE([Revenue by Category], [Total Revenue])
% Category Quantity = DIVIDE([Quantity by Category], [Total Pizzas Sold])
% Size Sales = DIVIDE([Revenue by Size], [Total Revenue])
% Size Quantity = DIVIDE([Quantity by Size], [Total Pizzas Sold])

#📊 Key Insights

Classic pizzas generate the highest revenue and order share.

Large pizzas contribute the most to overall sales.

Weekends (especially Friday & Saturday) see the maximum orders.

July and January show noticeable spikes in sales volume.

Top performers include multiple Chicken and Deluxe variants.

Lower performers are mostly Veggie and Mediterranean-style pizzas.

These insights help understand customer preferences, improvement areas, and sales seasonality.
