# 🚴‍♂️ Bike Store Revenue Analysis

## 📌 Project Overview
This project analyzes the revenue performance of a bike store using SQL and data visualization techniques. The goal is to uncover insights into sales trends, top customers, best-selling categories, and sales rep performance. By leveraging structured data from sales transactions, we can optimize decision-making and enhance business profitability.

## 📊 Dataset
The dataset consists of sales records from multiple stores, including details on revenue, product categories, customer purchases, and salesperson performance.

- **BikeStores2.xlsx**: Contains detailed sales data, including transaction history, product details, and customer information.
- **bike portfolio project.sql**: SQL queries used for data extraction, transformation, and analysis.
- **Dashboard 1.png**: A visual representation of the analysis, summarizing revenue trends and key performance indicators.

## 🔍 Key Insights
After analyzing the data, several important trends and insights were discovered:

- **Total revenue:** $8,578,989
- **Best-performing year:** 2017 recorded the highest revenue.
- **Revenue per category:**
  - Mountain Bikes: **$3,030,776** (35.33%)
  - Road Bikes: **$1,852,556** (21.59%)
  - Electric Bikes: **$1,020,237** (11.89%)
  - Cyclocross Bicycles: **$799,875** (9.32%)
  - Other categories also contributed significantly.
- **Top-performing store:** Baldwin Bikes generated **67.91%** of total revenue.
- **Highest sales rep performance:**
  - Marcelene Boyer: **$2,938,889**
  - Venita Daniel: **$2,887,353**
  - Other reps also contributed significantly.
- **Customer segmentation:**
  - Top customers like Pamelia Newman and Abby Gamble contributed significantly to sales.

## 📈 Analysis Process
The analysis followed a structured approach:
1. **Data Extraction** - Used SQL queries to extract relevant sales data.
2. **Data Cleaning & Transformation** - Processed data in Excel to ensure consistency.
3. **Data Analysis** - Performed aggregations and calculations to derive insights.
4. **Data Visualization** - Created dashboards in Tableau for better interpretation of trends.


  ## 🛠 Code Features
### 1️⃣ Extracting Revenue by Year
```sql
SELECT YEAR(order_date) AS Year, SUM(total_price) AS Revenue
FROM sales
GROUP BY YEAR(order_date)
ORDER BY Year DESC;
```
### 2️⃣ Identifying Top Customers
```sql
SELECT customer_name, SUM(total_price) AS Total_Spent
FROM sales
GROUP BY customer_name
ORDER BY Total_Spent DESC
LIMIT 10;
```
### 3️⃣ Sales Performance by Category
```sql
SELECT category_name, SUM(total_price) AS Revenue
FROM sales
JOIN products ON sales.product_id = products.product_id
GROUP BY category_name
ORDER BY Revenue DESC;
```
 

## 📂 Tools Used
To perform the analysis effectively, the following tools were utilized:
- **SQL** - For querying and extracting data from the database.
- **Excel** - For data preprocessing, cleaning, and basic analysis.
- **Tableau** - For visualizing data through interactive dashboards.🔗 Tableau: [[Dashboard](https://public.tableau.com/views/BikeStoreExecutiveDashboard_17429928677810/Dashboard1?:language=en-GB&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link))]

  ## 🏆 Future Improvements
- Optimize pricing strategies to maximize profitability.
- Identify underperforming sales reps and provide targeted training.
- Expand product offerings based on sales trends.

## 🚀 How to Use
1. Clone this repository.
2. Run `bike portfolio project.sql` in a SQL database environment to retrieve data.
3. Use `BikeStores2.xlsx` for further analysis in Excel.
4. Open `Dashboard 1.png` to view the visual insights.
5. Modify and build upon the provided analysis for further business insights.

## 📌 Author
[Nissi Douglas]  
📧 Contact: [Muanissidouglas@gmail.com]  
🔗 LinkedIn: [[Your Profile](https://www.linkedin.com/in/nissidouglas/)]

## 📢 Contributions
Contributions are welcome! Feel free to fork the repository, submit pull requests, and enhance the analysis with additional insights or improved visualizations.



