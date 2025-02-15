# E-commerce Data Analysis and Customer Behavior Insights

This project involves comprehensive data analysis on an e-commerce dataset to uncover customer behavior patterns, sales trends, product popularity, payment behaviors, and customer satisfaction. It employs Exploratory Data Analysis (EDA), data visualization, and segmentation techniques to gain actionable insights that can be leveraged for business growth and strategic decision-making.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Datasets](#datasets)
- [Objective](#objective)
- [Analysis and Insights](#analysis-and-insights)
  - [1. Exploratory Data Analysis (EDA)](#1-exploratory-data-analysis-eda)
    - [a. High-Level Metrics](#a-high-level-metrics)
    - [b. New Customer Acquisition](#b-new-customer-acquisition)
    - [c. Customer Retention](#c-customer-retention)
    - [d. Revenue Trends](#d-revenue-trends)
    - [e. Sales and Quantity Trends](#e-sales-and-quantity-trends)
    - [f. Popular Products](#f-popular-products)
    - [g. Popular Categories](#g-popular-categories)
    - [h. Top 10 Most Expensive Products](#h-top-10-most-expensive-products)
  - [2. Customer and Seller Segmentation](#2-customer-and-seller-segmentation)
    - [a. Customer Segmentation by Revenue](#a-customer-segmentation-by-revenue)
    - [b. Seller Segmentation by Revenue](#b-seller-segmentation-by-revenue)
  - [3. Cross-Selling Analysis](#3-cross-selling-analysis)
  - [4. Payment Behavior](#4-payment-behavior)
  - [5. Customer Satisfaction Analysis](#5-customer-satisfaction-analysis)
- [Technologies Used](#technologies-used)
- [Results and Insights](#results-and-insights)

---

## Project Overview
This project analyzes data from an e-commerce platform to:
- Understand customer acquisition, retention, and purchase behavior.
- Identify sales trends and seasonality by category, location, and time.
- Segment customers and sellers based on revenue.
- Uncover popular products and cross-selling opportunities.
- Analyze payment behavior and customer satisfaction levels.

---

## Datasets
The analysis utilizes the following datasets:
1. **Customers.csv** - Customer information including unique IDs and demographic details.
2. **Sellers.csv** - Seller details including unique seller IDs.
3. **Products.csv** - Product details including category names and product IDs.
4. **Orders.csv** - Order data with timestamps for purchase, approval, delivery, and estimated delivery.
5. **Order_Items.csv** - Details of items within orders including price and freight charges.
6. **Order_Payments.csv** - Payment details including payment methods and values.
7. **Order_Review_Ratings.csv** - Customer reviews and ratings for products.
8. **Geo_Location.csv** - Geographic location details, including state and city.

---

## Objective
- To perform detailed exploratory analysis and understand high-level metrics.
- To investigate customer acquisition, retention, and revenue trends.
- To identify popular products, categories, and cross-selling opportunities.
- To segment customers and sellers based on revenue generated.
- To analyze payment behavior and customer satisfaction.

---

## Analysis and Insights

### 1. Exploratory Data Analysis (EDA)

#### a. High-Level Metrics
Calculated the following high-level metrics:
- **Total Revenue:** $13,591,643.70  
- **Total Quantity Sold:** 112,650  
- **Total Products:** 32,951  
- **Total Categories:** 71  
- **Total Sellers:** 3,095  
- **Total Locations:** 19,015  
- **Total Payment Methods:** 5  

---

#### b. New Customer Acquisition
- Calculated the number of new customers acquired each month by:
  - Merging `Customers` and `Orders` datasets.
  - Identifying the first purchase date for each customer.
  - Grouping by month and visualizing the trend using bar charts.

---

#### c. Customer Retention
- Examined customer retention on a month-on-month basis:
  - Calculated the number of returning customers by subtracting new customers from total customers for each month.
  - Visualized retention trends using bar charts.

---

#### d. Revenue Trends
- Analyzed revenue from existing and new customers on a monthly basis by:
  - Calculating final price as the sum of product price and freight value.
  - Grouping by month and visualizing revenue trends.

---

#### e. Sales and Quantity Trends
Explored sales and quantity trends across:
- **Category:** Quantity and sales by product category.
- **Location:** Quantity and sales by state and city.
- **Time:** Analyzed trends by month, week, and day to identify seasonality and peak sales periods.
- **Payment Method:** Distribution of payment methods and their revenue contribution.

---

#### f. Popular Products
Identified popular products by:
- Grouping by seller and product ID to calculate product counts.
- Identifying the most popular products for each seller.

---

#### g. Popular Categories
- Analyzed popular product categories by state and month:
  - Grouped data by `year_month` and `product_category_name`.
  - Identified the most popular categories for each month.

---

#### h. Top 10 Most Expensive Products
- Listed the top 10 most expensive products by merging `Order_Items` and `Products` datasets and sorting by price.

---

### 2. Customer and Seller Segmentation

#### a. Customer Segmentation by Revenue
- Segmented customers into revenue groups using custom bins.
- Identified that the majority of customers spent between $0-$1k.

---

#### b. Seller Segmentation by Revenue
- Segmented sellers into revenue groups using custom bins.
- Identified revenue distribution among sellers.

---

### 3. Cross-Selling Analysis
- Investigated which products are frequently bought together:
  - Created product combinations for each order using `itertools.combinations`.
  - Counted the frequency of each combination.
  - Listed the top 10 most common product pairs.

---

### 4. Payment Behavior
- Analyzed payment behaviors by:
  - Identifying payment methods used by customers.
  - Determining the most popular payment channels by number of transactions and revenue.

---

### 5. Customer Satisfaction Analysis
- Analyzed customer satisfaction across multiple dimensions:
  - **Categories:** Top 10 maximum and minimum rated product categories.
  - **Products:** Top 10 maximum and minimum rated products.
  - **Location, Seller, and Month:** Average ratings by location, seller, and month.

---

## Technologies Used
- **Programming Language:** Python
- **Libraries Used:**
  - `Pandas`, `NumPy` for data manipulation and analysis.
  - `Matplotlib`, `Seaborn` for data visualization.
- **Tools:** Jupyter Notebook, GitHub for version control.

---

---

## Usage
1. Place the datasets (`CUSTOMERS.csv`, `SELLERS.csv`, `PRODUCTS.csv`, `ORDERS.csv`, `ORDER_ITEMS.csv`, `ORDER_PAYMENTS.csv`, `ORDER_REVIEW_RATINGS.csv`, `GEO_LOCATION.csv`) in the project directory.
2. Run the analysis scripts in Jupyter Notebook:
    ```bash
    jupyter notebook
    ```
3. Execute the notebooks in sequence to:
   - Perform Exploratory Data Analysis (EDA)
   - Conduct Customer and Seller Segmentation
   - Analyze Payment Behavior and Customer Satisfaction

---

## Results and Insights
- Discovered seasonal sales patterns and peak sales periods.
- Identified top-selling products and categories by location and time.
- Uncovered popular product combinations for cross-selling.
- Revealed customer and seller segmentation insights based on revenue.
- Analyzed payment preferences and customer satisfaction trends.

---
