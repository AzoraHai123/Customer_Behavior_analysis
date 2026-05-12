Customer Shopping Behavior — Data Analytics Project

Analyzing customer shopping patterns to uncover insights on revenue, product performance, and customer segmentation.


Overview
This project performs end-to-end data analysis on a customer shopping behavior dataset. It covers data loading, exploratory data analysis (EDA), data cleaning, SQL-based querying, Power BI dashboard creation, and a final presentation report.

Dataset
DetailInfoFilecustomer_shopping_behavior.csvRows~3,900 recordsKey Columnscustomer_id, age, gender, category, item_purchased, purchase_amount, review_rating, subscription_status, discount_applied, frequency_of_purchases

Tools Used
ToolPurposePython (pandas, sqlalchemy, pymysql)Data loading, EDA, cleaning, MySQL exportMySQL / MySQL WorkbenchDatabase storage, SQL queriesPower BI DesktopInteractive dashboard<img width="1883" height="907" alt="Screenshot 2026-05-12 185808" src="https://github.com/user-attachments/assets/2b2a63b2-a626-43a8-bd9c-d169fff65848" />
<img width="1883" height="907" alt="Screenshot 2026-05-12 185808" src="https://github.com/user-attachments/assets/5ef7e39d-75ee-4c31-8edf-06ce6018b227" />


Steps
1. Data Loading

Loaded CSV using pd.read_csv()
Previewed data with .head(), .info(), .describe()

2. Exploratory Data Analysis (EDA)

Checked data types and summary statistics
Identified missing values using .isnull().sum()

3. Data Cleaning

Imputed missing Review Rating values with median per category
Renamed columns to snake_case for consistency
Renamed purchase_amount_(usd) → purchase_amount
Created new column age_group using pd.qcut() (Young Adult, Adult, Middle-aged, Senior)
Created purchase_frequency_days by mapping frequency labels to numeric values
Dropped redundant column promo_code_used (identical to discount_applied)

4. MySQL Export

Connected Python to MySQL using SQLAlchemy + pymysql
Pushed cleaned DataFrame to MySQL table customer in database customer_behavior

5. SQL Queries
Ran 10 business queries including:

Revenue by gender
Discount customers spending above average
Top 5 products by average review rating
Shipping type vs average purchase amount
Subscriber vs non-subscriber spend comparison
Discount rate by product
Customer segmentation (New / Returning / Loyal)
Top 3 products per category using ROW_NUMBER()
Repeat buyers vs subscription status
Revenue contribution by age group

6. Power BI Dashboard

Imported cleaned data into Power BI
Created DAX measures: Total Revenue, Avg Spend, Total Customers, Discount Rate
Built visuals: bar charts, pie charts, line charts, slicers
Designed interactive dashboard with filters by gender, category, age group

