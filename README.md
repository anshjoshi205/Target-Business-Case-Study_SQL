#  🛒Target-Business-Case-Study_SQL 📊🇧🇷
![image](https://github.com/user-attachments/assets/8f1bdbc0-a2cc-402b-bf29-47bb117c45c8)

This business case focuses on the operations of Target in Brazil and provides Insights and recommendation by analyzing data of 100,000 orders placed between 2016 and 2018.


**📋Context:**

Target is a globally renowned brand and a prominent retailer in the United States. Target makes itself a preferred shopping destination by offering outstanding value, inspiration, innovation and an exceptional guest experience that no other retailer can deliver.

This particular business case focuses on the operations of Target in Brazil and provides insightful information about 100,000 orders placed between 2016 and 2018. The dataset offers a comprehensive view of various dimensions including the order status, price, payment and freight performance, customer location, product attributes, and customer reviews.

By analyzing this extensive dataset, it becomes possible to gain valuable insights into Target's operations in Brazil. The information can shed light on various aspects of the business, such as order processing, pricing strategies, payment and shipping efficiency, customer demographics, product characteristics, and customer satisfaction levels.

___________________________________________________________________________________________________________

** 📂Dataset:** https://drive.google.com/drive/folders/1TGEc66YKbD443nslRi1bWgVd238gJCnb?usp=drive_link

The data is available in 8 csv files:

1.customers.csv
2.sellers.csv
3.order_items.csv
4.geolocation.csv
5.payments.csv
6.reviews.csv
7.orders.csv
8.products.csv
___________________________________________________________________________________________________________

The column description for these csv files is given below.
🧑‍💻

The **customers.csv** contain following features:

| **Feature**                     | **Description**                                                   |
|----------------------------------|-------------------------------------------------------------------|
| customer_id                     | ID of the consumer who made the purchase                         |
| customer_unique_id              | Unique ID of the consumer                                         |
| customer_zip_code_prefix        | Zip Code of consumer’s location                                   |
| customer_city                   | Name of the City from where order is made                         |
| customer_state                  | State Code from where order is made (Eg. São Paulo - SP)         |

The **sellers.csv** contains following features:

| **Feature**                     | **Description**                                                   |
|----------------------------------|-------------------------------------------------------------------|
| seller_id                       | Unique ID of the seller registered                                |
| seller_zip_code_prefix          | Zip Code of the seller’s location                                 |
| seller_city                      | Name of the City of the seller                                    |
| seller_state                     | State Code (Eg. São Paulo - SP)                                   |

The **order_items.csv** contain following features:

| **Feature**                     | **Description**                                                   |
|----------------------------------|-------------------------------------------------------------------|
| order_id                        | A Unique ID of order made by the consumers                        |
| order_item_id                   | A Unique ID given to each item ordered in the order               |
| product_id                      | A Unique ID given to each product available on the site           |
| seller_id                       | Unique ID of the seller registered in Target                      |
| shipping_limit_date             | The date before which the ordered product must be shipped         |
| price                           | Actual price of the products ordered                              |
| freight_value                   | Price rate at which a product is delivered from one point to another|


The **geolocations.csv** contain following features:

| **Feature**                     | **Description**                                                   |
|----------------------------------|-------------------------------------------------------------------|
| geolocation_zip_code_prefix     | First 5 digits of Zip Code                                        |
| geolocation_lat                  | Latitude                                                          |
| geolocation_lng                  | Longitude                                                         |
| geolocation_city                 | City                                                              |
| geolocation_state                | State                                                             |

The **payments.csv** contain following features:

| **Feature**                     | **Description**                                                   |
|----------------------------------|-------------------------------------------------------------------|
| order_id                        | A Unique ID of order made by the consumers                        |
| payment_sequential               | Sequences of the payments made in case of EMI                     |
| payment_type                    | Mode of payment used (Eg. Credit Card)                            |
| payment_installments             | Number of installments in case of EMI purchase                    |
| payment_value                    | Total amount paid for the purchase order                          |


The **orders.csv** contain following features:

| **Feature**                     | **Description**                                                   |
|----------------------------------|-------------------------------------------------------------------|
| order_id                        | A Unique ID of order made by the consumers                        |
| customer_id                     | ID of the consumer who made the purchase                         |
| order_status                    | Status of the order made i.e. delivered, shipped, etc.            |
| order_purchase_timestamp        | Timestamp of the purchase                                         |
| order_delivered_carrier_date    | Delivery date at which carrier made the delivery                  |
| order_delivered_customer_date   | Date at which customer got the product                            |
| order_estimated_delivery_date   | Estimated delivery date of the products                           |

The **reviews.csv** contain following features:

| **Feature**                     | **Description**                                                   |
|----------------------------------|-------------------------------------------------------------------|
| review_id                       | ID of the review given on the product ordered by the order id     |
| order_id                        | A Unique ID of order made by the consumers                        |
| review_score                    | Review score given by the customer for each order on a scale of 1-5|
| review_comment_title            | Title of the review                                               |
| review_comment_message          | Review comments posted by the consumer for each order            |
| review_creation_date            | Timestamp of the review when it is created                        |
| review_answer_timestamp         | Timestamp of the review answered                                  |


The **products.csv** contain following features:

| **Feature**                     | **Description**                                                   |
|----------------------------------|-------------------------------------------------------------------|
| product_id                      | A Unique identifier for the proposed project                      |
| product_category_name            | Name of the product category                                      |
| product_name_length             | Length of the string which specifies the name given to the products|
| product_description_length      | Length of the description written for each product ordered on the site |
| product_photos_qty              | Number of photos of each product ordered available on the shopping portal |
| product_weight_g                | Weight of the products ordered in grams                           |
| product_length_cm               | Length of the products ordered in centimeters                     |
| product_height_cm               | Height of the products ordered in centimeters                     |
| product_width_cm                | Width of the product ordered in centimeters                       |

___________________________________________________________________________________________________________

Dataset schema:
![image](https://github.com/user-attachments/assets/1312ab05-636c-4d02-aae6-d7edb5683671)

___________________________________________________________________________________________________________

## Problem Statement

As a Data Analyst/Scientist at Target, you are tasked with analyzing the provided dataset to extract valuable insights and provide actionable recommendations for improving operations, customer satisfaction, and the overall business strategy. The dataset contains various tables related to customer orders, payments, and delivery details.

### 🔎Tasks

1. **Initial Data Exploration**

   - **1.1. Data Types & Structure**
     - Check the data type of all columns in the `customers` table.
   
   - **1.2. Time Range of Orders**
     - Get the time range between which the orders were placed.

   - **1.3. Customer Distribution**
     - Count the number of customers from each city and state who placed orders during the given period.

2. **In-depth Exploration**

   - **2.1. Orders Trend**
     - Analyze if there is a growing trend in the number of orders placed over the past years.

   - **2.2. Monthly Seasonality**
     - Identify if there is any seasonal trend (monthly) in the number of orders being placed.

   - **2.3. Brazilian Customer Behavior**
     - Determine the time of day when Brazilian customers mostly place their orders. Categorize the time into:
       - 0-6 hrs : Dawn
       - 7-12 hrs : Morning
       - 13-18 hrs : Afternoon
       - 19-23 hrs : Night

3. **Evolution of E-commerce Orders in Brazil**

   - **3.1. Month-on-Month Orders**
     - Get the month-on-month number of orders placed in each state.

   - **3.2. Customer Distribution**
     - Analyze how customers are distributed across different states in Brazil.

4. **Impact on Economy: Cost Analysis**

   - **4.1. Yearly Cost Comparison**
     - Calculate the percentage increase in the cost of orders from 2017 to 2018 (Include months between Jan and Aug only).
     - Use the `payment_value` column in the `payments` table to calculate the cost of orders.

   - **4.2. State-wise Order Analysis**
     - Calculate the total and average order price for each state.
     - Calculate the total and average freight cost for each state.

5. **Analysis Based on Sales, Freight, and Delivery Time**

   - **5.1. Delivery Time Calculation**
     - Calculate the number of days taken to deliver each order from the purchase date as `delivery_time`.
     - Calculate the difference (in days) between the estimated and actual delivery date of an order.

   - **5.2. Delivery Time Analysis**
     - Identify the top 5 states with the highest and lowest average freight value.
     - Identify the top 5 states with the highest and lowest average delivery time.
     - Identify the top 5 states where the order delivery is faster than expected (compared to the estimated delivery date).

6. **Analysis Based on Payments**

   - **6.1. Monthly Payment Type Usage**
     - Find the month-on-month number of orders placed using different payment types.

   - **6.2. Payment Installments Analysis**
     - Analyze the number of orders placed based on the payment installments made.

---
___________________________________________________________________________________________________________
