# SQL-RESTAURANT-DATA-ANALYSIS
This project contains SQL queries to analyze customer and sales data for a fictional restaurant. The queries answer various business-related questions, including customer spending habits, popular menu items, and loyalty program behavior.

# STEPS TAKEN
## Data Preparation
 - Database and Table Creation:

- Created a database named projects.
- Defined three key tables:
- sales to track customer purchases, including customer_id, order_date, and product_id.
- menu to store menu items with their names and prices.
- members to capture customer membership details, including the date they joined.

## Data Analysis
I addressed various business questions by writing SQL queries:

### Q1: What is the total amount each customer spent in the restaurant?
- Joined sales and menu tables on product_id to associate each purchase with its price.
- Aggregated the data to calculate total spending for each customer.

### Q2: How many days has each customer visited the restaurant?
- Counted distinct order_date entries for each customer in the sales table.
- Highlighted customers with frequent visits.

### Q3: What was the first item purchased by each customer?
- Used a Common Table Expression (CTE) to identify the earliest purchase date for each customer.
- Joined the result with the menu table to extract the corresponding product.

### Q4: What is the most purchased item on the menu, and how many times was it purchased?
- Counted the frequency of each product_id in the sales table.
- Ordered the results to determine the most purchased item.

### Q5: Which item was the most popular for each customer?
- Calculated the purchase frequency for each item per customer.
- Used DENSE_RANK() to rank items based on popularity for each customer.

### Q6: What was the first item purchased by the customer after joining the membership program?
- Identified the first purchase date after the membership join date using a CTE.
- Matched this date with the menu table to extract the product name.

### Q7: What was the last item purchased by the customer before becoming a member?
- Found the last purchase date before the join date using a CTE.
- Joined the result with the menu table to identify the product.

### Q9: How many items and how much did each customer spend before becoming a member?
- Filtered purchases made before the join date.
- Summed item counts and total spending per customer.

### Q9: How many loyalty points does each customer have?
- Used a CASE statement to apply the points multiplier based on item type.
- Aggregated the points for each customer.

### Q10: How many points would customers earn in their first week of membership?
- Identified purchases within the first 7 days after joining.
- Applied a double-points multiplier for all items during this period.

## Technologies Used
Database Management System: MySQL

## Outcomes
- Delivered actionable insights into customer behavior and menu popularity.
- Simulated the impact of promotional offers, such as loyalty programs.
- Provided a framework for data-driven decision-making in restaurant management.
