**📦 Smart Last-Mile Delivery Optimization (Zepto-style Analytics Case Study)**

**🧠 Business Problem**

In hyperlocal delivery platforms like Zepto, Blinkit, and Instamart, last-mile delivery is the most cost-intensive and delay-prone stage of logistics.

The company faces challenges such as:

Increasing delivery delays in specific zones

Inefficient driver routing and fuel usage

Lack of visibility into operational bottlenecks

Inconsistent on-time delivery performance


**🎯 Objective**

To build an end-to-end analytics solution that:

Improves delivery efficiency

Reduces delay rate

Optimizes driver and fuel performance

Identifies operational bottlenecks using data-driven insights


**🛠️ Tech Stack**

SQL (MySQL) → Data storage, cleaning, KPI calculations

Power BI → Dashboard development & visualization

DAX → KPI calculations and business metrics

Power Query → Data transformation & modeling


**📊 Key Business KPIs**

| KPI                   | Description                   |
| --------------------- | ----------------------------- |
| Total Orders          | 12,900+ deliveries analyzed   |
| On-Time Delivery Rate | 97.63% operational efficiency |
| Delayed Orders        | 1,961 late deliveries         |
| Avg Delivery Time     | 44.49 minutes                 |
| Distance Covered      | 165,000+ km                   |


**📌 Dashboard Highlights (Power BI)**

📍 1. Delivery Performance Overview

On-time vs delayed delivery tracking
SLA performance by zone

🚦 2. Delay Root Cause Analysis

Traffic, Weather, Address Issues, Vehicle breakdowns
Location-wise delay heatmap

⛽ 3. Fuel Efficiency Analysis

Fuel usage vs distance scatter analysis
Identification of inefficient routes

🧑‍✈️ 4. Driver Performance Dashboard

Top vs low-performing drivers
Delivery speed comparison

📈 5. Trend Analysis

Quarterly delivery time variation
Seasonal operational performance shifts


**🧮 DAX Measures Used**

OnTime Delivery % =
DIVIDE(
    CALCULATE(COUNT(delivery[id]), delivery[status] = "Ontime"),
    COUNT(delivery[id]))

Average Delivery Time =
AVERAGE(delivery[delivery_minutes])

Delay Count =
CALCULATE(COUNT(delivery[id]), delivery[status] = "Late")


**🗄️ SQL Contributions**

Data cleaning and transformation

KPI table creation

Aggregation by:
Location

Driver

Time period

Performance optimization for reporting


**📈 Key Business Insights**

🔴 Key Business Insights

✔ Certain high-density zones show consistently higher delay rates despite high demand, indicating congestion-driven inefficiencies in route planning

✔ Traffic congestion and incorrect address entries are the primary controllable drivers of delivery delays

✔ Short-distance trips show higher operational inefficiency in terms of delivery time per km, indicating suboptimal route allocation patterns

✔ Seasonal spikes in delivery time suggest capacity constraints during peak demand periods

✔ Significant performance gap between top and low-performing drivers affects overall SLA consistency


💡 Business Recommendations

✔ Implement dynamic route optimization system

✔ Introduce driver performance scoring system

✔ Improve address validation at order entry stage

✔ Optimize driver allocation in high-delay zones

✔ Use predictive analytics for peak season planning


****📌 Executive Impact: ****

📌 Executive Impact:

This solution enables a shift from reactive logistics monitoring to proactive, KPI-driven operational optimization by improving route efficiency, reducing delivery delays, and enhancing driver performance visibility.
