# LITA SALES DATA PROJECT
### PROJECT TITLE: SALES ANALYSIS FOR AN APPAREL AND ACCESSORIES BRAND

---

[Project Overview for Sales Data](#project-overview-for-sales-data)

[Data Sources](#data-sources)

[Key Features for Sales Data](#key-features-for-sales-data)

[Technologies Used](#technologies-used)

[Data Cleaning and Preparations](#data-cleaning-and-preparations)

[Exploratory Data Analysis (EDA) for Sales data ](#exploratory-data-analysis-(eda)-for-sales-data-and-customer-subscription-data)

[Data Analysis](#data-analysis)

[Data Visualization for Sales Data](#data-visualization-for-sales-data)

[Results and Insights for Sales Data](#results-and-insights-for-sales-data)

[Recommendations for Sales Data](#recommendations-for-sales-data)

---

### Project Overview for Sales Data
This project analyses a dataset containing sales data for various apparel and accessories, including shirts, shoes, gloves, jackets, hats, and socks. The datasets include key information such as product types, order IDs, customer IDs, quantity of products sold, and unit prices. the primary objective of this project is to uncover insights from the sales data that can help this business brand make informed decisions to improve its product offerings, sales strategies, and customer experience.

---

### Data Sources
The primary source of data used here is Data Sale.CSV. It is open-source data that can be freely downloaded from an open source online such as Kaggle, FRED or any other data repository site. 

---

### Key Features for Sales Data

I. Order ID: Unique identifier for each order, enabling precise tracking and management of transactions.

ii. Order Date: The date when the order was placed, allowing for time-based analysis of sales trends and seasonal patterns.

iii. Customer ID: Unique identifier for each customer, facilitating customer segmentation and analysis of purchasing behaviours.

iv. Revenue: Total income generated from each order, providing insights into financial performance and profitability.

v. Quantity: Number of units sold in each order, which helps assess product demand and inventory management.

vi. Unit Price: Price per individual item sold, useful for calculating revenue per product and understanding pricing strategies.

vii. Region: The geographic area where the order was placed, enabling regional sales analysis and targeted marketing efforts.

viii. Product: Description or name of the product sold, allowing for analysis of product performance and popularity within the sales data.

These features collectively provide a comprehensive view of sales performance, customer behaviour, and regional trends, enabling informed decision-making for marketing strategies, inventory management, and overall business growth.


---

### Technologies Used
- Microsoft Excel [Download here](https://www.microsoft.com)
  1. For Data Cleaning
  2. For Analysis
  3. For Data  Visualization
- SQL-  Structured Query Language
  1. For querying of data.
  2. For storing data.
  3. For managing data and,
  4. For manipulating data.
- POWER BI
  1.  For beautiful and interactive data visualizations.
  2.  For insightful data reports.
  3.  For retrieving data from different sources.
- Github
  1. For Portfolio Building.
  2. For collaboration and teamwork

  Therefore, this project aims to equip stakeholders of the brand with actionable insights to enhance sales strategies, boost customer retention, and streamline inventory management.
  
---

### Data Cleaning and Preparations

In the initial phase of the data cleaning and preparations, the following actions were performed on the different technologies used;

#### Excel
  1. Data loading and inspection
  2. Handling missing and null variables using ISBLANK function in Excel
  3. Eliminating duplicates.
  4. Data cleaning and formatting.

#### SQL
  1. The already cleaned data from Excel was converted to a CSV file format, which enabled the data to be imported into SQL quickly and efficiently as opposed to directly importing an Excel file format.
  2. Creation of a database.

      ```SQL
          CREATE DATABASE LITA_PROJECT
      ```

     The above code creates a database that houses all tables ready for querying.
     
  4. Import the SalesData and CustomerData data into the already created database.
  5. Writing amazing codes to show the different trends and patterns in the dataset for making sound decisions.

#### POWER BI
  1. launched the power bi environment.
  2. Importation of both datasets using the TEXT/CSV file extension.
  3. Explored and cleaned the dataset.
  4. Confirmed the integrity of the datasets by using column quality, column distribution, and column profile options under the view tab.

---

### Exploratory Data Analysis (EDA) for Sales Data 
EDA involves exploring the data to answer some questions about the data such as;
- What is the overall sales trend
- Which products are top sellers
- What are the products on peak sales?

  ![Alt text for image](https://github.com/Light63/DATA_ANALYSIS_JOURNEY-_WITH_LITA/blob/main/Excel%20sales%20data%201.JPG?raw=true)

  Figure 1: Shows the overall trend sales for the sales data using pivot tables and charts


  ![Alt text for image](https://github.com/Light63/DATA_ANALYSIS_JOURNEY-_WITH_LITA/blob/main/BI%201.JPG?raw=true)







  Figure 2: Shows the already prepared dataset ready for visualizations. this is particularly important as it enables effective analysis of the data to make valid and informed 
  decisions that will in turn, identify patterns, and sales trends, as well as boost productivity. Hence, increasing revenue and customer satisfaction.


---

  ### Data Analysis
  The images  and codes below show how data analysis was performed on the datasets using the above-mentioned tools.

  ```SQL
  SELECT * FROM TABLE 1
  WHERE CONDITION = TRUE
  ```


 ```
create database LITA
```

1. TOTAL SALES FOR EACH PRODUCT CATEGORY

```
SELECT Product,
sum (sales_Revenue) As Total_sales
from SalesData_Project
group by product
```

2. Number of sales transactions in each region

```
select Region,
count (sales_Revenue) as number_sales_of_transactions
from SalesData_Project
group by Region
```

3. The highest-selling product by total sales value

```
select Top 1 product,
sum(sales_Revenue) as total_sales_value
from SalesData_Project
group by product
order by total_sales_value desc
```

4. calculate total revenue by product

```
select product, sum (sales_Revenue) as total_Revenue
FROM SalesData_Project
GROUP BY product
order by total_revenue 
```

5. calculate monthly sales totals for the current year

```
SELECT FORMAT(OrderDate, 'yyyy-MM') AS Month, SUM(sales_Revenue) AS Total_Sales
FROM SalesData_Project
WHERE OrderDate >= DATEFROMPARTS(YEAR(GETDATE()), 1, 1) -- Start of the current year
  AND OrderDate < DATEADD(YEAR, 1, DATEFROMPARTS(YEAR(GETDATE()), 1, 1)) -- Start of the next year
GROUP BY FORMAT(OrderDate, 'yyyy-MM')
ORDER BY Month
```

6. Top 5 customers by total purchase amount

```
select top 5(Customer_id),
sum (sales_Revenue) as total_purchase_amount
from SalesData_Project
group by Customer_Id
order by total_purchase_amount desc
```

7. calculate the percentage of total sales contributed by each region

```
select region,
sum (sales_Revenue) as total_sales,
round ((select sum (sales_Revenue)/ cast((select sum(sales_Revenue) 
from  SalesData_Project) as float) *100), 0) as 
percentage_total_sales
from SalesData_Project
group by region
order by region desc
```

8. identify products with no sales in the last quarter

```
SELECT DISTINCT Product
FROM SalesData_Project
WHERE Product NOT IN (
    SELECT Product
    FROM SalesData_Project
    WHERE OrderDate >= DATEADD(QUARTER, -1, GETDATE())
)
```

### Data Visualization for sales data


![ALT text for image](https://github.com/Light63/DATA_ANALYSIS_JOURNEY-_WITH_LITA/blob/main/BI%20SALES%20DATA%201.JPG?raw=true)


Figure 3: Shows the sales overview, highlighting the trends and patterns of customers in different regions. It also gives insights into the fact that shoes are in high demand while the demand for socks and jackets dwindles.

---

### Results and Insights for Sales Data

The analysis reveals that the total revenue generated stands at 2 million Naira, highlighting robust financial performance for the brand. The top-performing product identified is shoes, with a total quantity sold of 68,461 units. Regionally, the South leads in sales, followed by the East, North, and West. This indicates a strong network of loyal and returning customers in the South, as well as a notably high demand for shoes compared to other product categories offered by the brand.

---

### Recommendations  for Sales Data

Expand Shoe Offerings: Given the strong sales performance of shoes, consider expanding the product line to include variations such as different styles, colours, and limited editions to capture a larger market share.

Targeted Marketing Campaigns in the South: Leverage the high demand in the South by developing targeted marketing campaigns. Highlight shoe promotions and pair them with related accessories like socks or insoles to enhance the overall value proposition.

Cross-Selling Opportunities: Promote cross-selling strategies by bundling shoes with complementary products like jackets, hats, and gloves. This could incentivize customers to explore a wider range of offerings while increasing the average order value.

Regional Promotions: Consider implementing region-specific promotions to boost sales in the East, North, and West, where demand may not be as strong. Tailoring marketing efforts to the unique preferences and buying behaviours of customers in these regions can drive engagement.

Customer Feedback Mechanism: Establish a system for gathering customer feedback on the product range, particularly for jackets, hats, gloves, and shirts. This insight can inform future product development and ensure alignment with customer preferences.

By implementing these strategies, the brand can capitalize on the success of its shoe sales while also promoting a broader range of products, ultimately driving growth and enhancing customer loyalty.


---

