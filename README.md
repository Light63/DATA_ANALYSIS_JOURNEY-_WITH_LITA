# DATA_ANALYSIS_JOURNEY-_WITH_LITA
### PROJECT TITLE: SALES AND CUSTOMER DATA ANALYSIS FOR AN APPAREL AND ACCESSORIES BRAND

---

[Project Overview for Sales Data](#project-overview-for-sales-data)

[Project Overview for Customer Subscription Data](#project-overview-for-customer-subscription- data)

[Data Sources](#data-sources)

[Key Features for Sales Data](#key-features-for-sales-data)

[Key Features for Customer Subscription Data](#key-features-for-customer-subscription-data)

[Technologies Used](#technologies-used)

[Data Cleaning and Preparations](#data-cleaning-and-preparations)

[Exploratory Data Analysis (EDA) for Sales data and Customer Subscription Data](#exploratory-data-analysis-(eda)-for-sales-data-and-customer-subscription-data)

[Data Analysis](#data-analysis)

[Data Visualization for Sales Data](#data-visualization-for-sales-data)

[Data Visualization for Customer Subscription Data](#data-visualization-for-customer-subscription-data)

---

### Project Overview for Sales Data
This project analyses a dataset containing sales and customer data for various apparel and accessories, including shirts, shoes, gloves, jackets, hats, and socks. The datasets include key information such as product types, order IDs, customer IDs, quantity of products sold, and unit prices. the primary objective of this project is to uncover insights from the sales data that can help this business brand make informed decisions to improve its product offerings, sales strategies, and customer experience.

---

### Project Overview for Customer Subscription Data
This project analyses a dataset containing sales and customer data for various apparel and accessories, including shirts, shoes, gloves, jackets, hats, and socks. The datasets include key information such as product types, order IDs, customer IDs, quantity of products sold, and unit prices. the primary objective of this project is to uncover insights from the sales data that can help this business brand make informed decisions to improve its product offerings, sales strategies, and customer experience.

---

### Data Sources
The primary source of data used here is Data Sale.CSV. It is open-source data that can be freely downloaded from an open source online such as Kaggle or FRED or any other data repository site. 

---

### Key Features for Sales Data

#### Data Exploration and Cleaning: 
Assessing and cleaning the dataset to ensure accurate and reliable analysis.

#### Sales Performance Analysis: 
Analyzed sales trends for each product type using amazing tools like Excel, SQL, and Power Bid to identify the most popular products and seasonal patterns.

#### Customer Segmentation: 
Grouping customers based on their purchasing behaviour to understand preferences and tailor marketing strategies.

#### Order Analysis: 
Evaluating order details to determine order frequency, size, and trends across different product categories.

#### Visualizations:
Creating visualizations to present sales performance, customer segmentation, and trends for better decision-making.

---

### Key Features for Customer Subscription Data

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
  5. Writing amazing codes to show the different trends and patterns in the dataset for making sound decisions (screenshot of the codes).

#### POWER BI
  1. launched the power bi environment.
  2. Importation of both datasets using the TEXT/CSV file extension.
  3. Explored and cleaned the dataset.
  4. Confirmed the integrity of the datasets by using column quality, column distribution, and column profile options under the view tab(screenshot of this).

---

### Exploratory Data Analysis (EDA) for Sales Data and Customer Subscription Data 
EDA involves exploring the data to answer some questions about the data such as;
- What is the overall sales trend
- Which products are top sellers
- What are the products on peak sales? (pivot tables and charts for both datasets here)

  ![Alt text for image](https://github.com/Light63/DATA_ANALYSIS_JOURNEY-_WITH_LITA/blob/main/Excel%20sales%20data%201.JPG?raw=true)

  Figure 1: Shows the overall trend sales for the sales data using pivot tables and charts


  ![Alt text for image](https://github.com/Light63/DATA_ANALYSIS_JOURNEY-_WITH_LITA/blob/main/EXCEL%20CUSTOMER%20DATA.JPG?raw=true)


  Figure 2: Shows the overall trend sales  for the customer subscription data using pivot tables and charts




  ![Alt text for image](https://github.com/Light63/DATA_ANALYSIS_JOURNEY-_WITH_LITA/blob/main/BI%201.JPG?raw=true)







  Figure 3: Shows the already prepared dataset ready for visualizations. this is particularly important as it enables effective analysis of the data to make valid and informed decisions 
            that will in turn, identify patterns, and sales trends, as well as boost productivity. Hence, increasing revenue and customer satisfaction.


---

  ### Data Analysis
  the images  and codes below show how data analysis was performed on the datasets using the above-mentioned tools.

  ```SQL
  SELECT * FROM TABLE 1
  WHERE CONDITION = TRUE
  ```

---

### Data Visualization for sales data
(power bi visualizations)

![ALT text for image](https://github.com/Light63/DATA_ANALYSIS_JOURNEY-_WITH_LITA/blob/main/BI%20SALES%20DATA%201.JPG?raw=true)


Figure 4: Shows the sales overview, highlighting the trends and patterns of customers in different regions. It also gives insights into the fact that shoes are in high demand while the demand for socks and jackets dwindles.


###  Data Visualization for Customer Subscription Data
