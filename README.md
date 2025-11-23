# Excel Swiggy Dashboard
![swiggy_dashboard](https://github.com/user-attachments/assets/bcb604d7-0057-4ead-aa46-426067e163f6)

## Introduction
This dashboard provides insights into Swiggy’s food sales, user ratings, and total order distribution across India.

### Excel Skills Used

The following Excel skills were utilized for analysis:

- **🎯 Key Performance Indicator(KPI)**
- **📉 Charts**
- **🧮 Formulas and Functions**

### Swiggy Dataset

The dataset used for this project contain real-time swiggy order from 2025. This dataset provides a foundation for analyzing data using Excel. It includes detailed information on:

- **🗺️ State**
- **📆 Order Date**
- **🗂️ Category**
- **🥗 Dish Name**
- **💰 Price**

## Dashboard Build


### 🎯 Key Performance Indicator(KPI)

<img width="511" height="75" alt="kpi&#39;s" src="https://github.com/user-attachments/assets/514331ba-bdeb-461f-a38d-853a0efa7b2d" />

- **💰Total Sales**: Represents the total revenue generated from all completed customer orders.
- **⭐ Average Rating**: Shows the overall customer satisfaction level based on the average rating score.
- **🧐 Total Review**: Indicates the total number of customer reviews or feedback entries submitted.
- **📦 Total Orders**: Displays the total count of customer orders placed during the selected period.
- **💸 AOV (Average Order Value)**: Measures the average amount spent per order by dividing total sales by total orders.

### 📉 Charts 

#### 📈 Monthly Sales Trend - Line Chart

<img width="622" height="238" alt="monthly_sales" src="https://github.com/user-attachments/assets/522405c2-e0a6-41f3-8171-1072a2c89bcb" />

- 🛠️ **Excel Features:** Leveraged line chart with markers and customized currency formatting (₹K format) for better readability.
- 🎨 **Design Choice:** A smooth line visualization was selected to clearly reflect month-over-month sales fluctuations.
- 📅 **Time-Based Analysis:** Displays monthly sales performance across the year to help identify seasonal patterns.
- 💡 **Insights Gained:** Sales peaked in Jan while Feb showed the lowest performance, indicating potential seasonal buying behavior or promotional impact.

#### ◔ Sales by Food Type - Pie Chart
<img width="294" height="244" alt="pie_chart" src="https://github.com/user-attachments/assets/f62cd59c-2a9a-45a5-8db1-441ec61d2f63" />

- 🛠️ **Excel Features:** Created a doughnut chart with data labels displaying both value (₹) and percentage for clarity.
- 🎨 **Design Choice:** A clean doughnut chart was used to visually highlight proportional contribution between Veg and Non-Veg categories.
- 🍽️ **Category Comparison:** The chart compares total sales generated from Veg and Non-Veg menu items.
- 💡 **Insights Gained:** Non-Veg contributes the majority share at 64%, while Veg accounts for 36%, indicating stronger demand and revenue from Non-Veg items.

#### 🌍 State-wise Sales Analysis - Map Chart
<img width="417" height="528" alt="india map" src="https://github.com/user-attachments/assets/a352115a-1dfa-448d-9176-277f6e61dcd6" />


- 🛠️ **Excel Features:** Used a filled map chart with geographic data mapping to visualize state-level performance.
- 🎨 **Design Choice:** Applied a gradient color scale to represent low-to-high sales regions, making differences easily noticeable.
- 📍 **Regional Comparison:** Highlights how sales vary across Indian states, enabling quick identification of high-performing and underperforming regions.
- 💡 **Insights Gained:** Southern and Western states show significantly higher sales contributions, while Northeastern regions reflect comparatively lower demand.

#### 📊 Daily Sales Trend - Bar Chart

<img width="615" height="232" alt="daily sales analysis" src="https://github.com/user-attachments/assets/461bc15e-76ae-465c-8756-e0f4487270a4" />

- 🛠️ **Excel Features:** Created a vertical bar chart with formatted currency labels to visualize daily sales performance.
- 🎨 **Design Choice:** A gradient color style was applied to highlight variations between weekdays and weekends.
- 📊 **Pattern Recognition:** Displays sales values across each day of the week to identify consistent highs or lows.
- 💡 **Insights Gained:** Saturday records the highest sales, while early weekdays like Monday and Tuesday show comparatively lower performance, indicating stronger weekend demand.

#### ⊞ Quarterly Sales, Rating & Orders Summary 
<img width="303" height="245" alt="total_sales by each quarter" src="https://github.com/user-attachments/assets/2f37a6b1-b95f-42fe-b3ba-fcff4c62f475" />

- 🛠️ **Excel Features:** Utilized conditional formatting and structured table formatting to enhance readability and data interpretation.
- 🎨 **Design Choice:** Applied color-based data highlights to emphasize performance differences across quarters for sales, orders, and ratings.
- 📅 **Quarterly Breakdown:** Presents key performance figures (Sales, Rating, and Order Count) across Q1, Q2, and Q3 to support comparative analysis.
- 💡 **Insights Gained:** Q2 shows the strongest performance with the highest sales and orders, while Q3 reflects a noticeable decline despite consistent customer ratings.

#### 🌆 Top 5 Cities by Sales - Bar Chart

<img width="388" height="229" alt="top 5 city" src="https://github.com/user-attachments/assets/40f23d2a-906d-4b65-9a86-a239e0abb602" />


- 🛠️ **Excel Features:** Created a horizontal bar chart with data labels formatted in currency for clear comparison.
- 🎨 **Design Choice:** A ranked layout with uniform color gradients helps visualize sales hierarchy across cities.
- 🏙️ **City-Level Comparison:** Highlights the top-performing cities based on total revenue contribution.
- 💡 **Insights Gained:** Bengaluru leads significantly in sales, while Lucknow, Hyderabad, Mumbai, and New Delhi follow closely with moderate performance levels.

#### 📆 Weekly Sales Trend - Bar Chart
<img width="980" height="234" alt="weeknumbers" src="https://github.com/user-attachments/assets/d9fcb7e4-9f49-4174-b0f0-a190a07919fc" />

- 🛠️ **Excel Features:** Used a continuous bar chart with formatted currency scaling to visualize weekly sales distribution across the dataset.
- 🎨 **Design Choice:** A uniform color style was applied to maintain consistency while allowing weekly variations to stand out clearly.
- 📊 **Trend Monitoring:** Displays sales figures for each week, helping track performance patterns and identify any sudden spikes or drops.
- 💡 **Insights Gained:** While most weeks maintain consistent sales levels, Week 8 shows a noticeable peak whereas the final week indicates a sharp drop, suggesting potential seasonality or end-of-period impact.


### 🧮 Formulas and Functions 

#### 🍽️ Food Type Classification Logic
```
=IF(OR(
ISNUMBER(SEARCH("chicken",H3)),
ISNUMBER(SEARCH("egg",H3)),
ISNUMBER(SEARCH("fish",H3)),
ISNUMBER(SEARCH("mutton",H3)),
ISNUMBER(SEARCH("prawn",H3)),
ISNUMBER(SEARCH("biryani",H3)),
ISNUMBER(SEARCH("kabab",H3)),
ISNUMBER(SEARCH("kebab",H3)),
ISNUMBER(SEARCH("Non-Veg",H3)),
ISNUMBER(SEARCH("non veg",H3))
),"Non-Veg" ,"Veg")
```


- *To categorize each food item as **Veg** or **Non-Veg**, a conditional formula was applied in Excel using keyword-based text detection. The logic checks if the item description contains any non-vegetarian keywords (such as *chicken, egg, fish, mutton, prawn, biryani, kabab/kebab,* or related terms*).*  
- If a match is found, the entry is labeled as **"Non-Veg"**; otherwise, it is assigned to the **"Veg"** category.


## Conclusion
I created this dashboard to analyze food delivery trends based on Swiggy-style order data and uncover meaningful business insights. By exploring patterns across food type preferences, sales performance, order distribution, customer ratings, and regional variations, this dashboard helps users understand how customer behavior, geography, and product categories influence overall revenue.
