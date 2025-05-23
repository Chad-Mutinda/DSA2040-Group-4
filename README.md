
# Retail Data Warehouse

This project builds a mini data warehouse for a fictional retail company to analyze sales performance by product, store, and time.

## Contents

- `schema2.sql`: Table creation scripts
- `Queries2.sql`: Sample analytical queries
- `*.csv`: Dimension and fact data
- Screen shots showings the outputs of the sample analytical queries

## Loading the data sets
We used MySQL for the work and for loading  the data sets, we made use of the table data import wizard.

## Team Members

- Sevidzem Marilyn 669229(@marilynmaika)
- Hetal Kumbharana -670207 (@HetalK4)
- Chad Mutinda (@Chad-Mutinda)
- Mangu Rita (@ritzy10)


## License

MIT License


# Part 5: Reflection & Discussion
Discussion Questions:
# Q1 Why use a star schema instead of a normalized schema?
A normalized schema involves breaking down a large table into several smaller tables. Each small table has its own primary key. Foreign keys are used to establish relationships between the tables. 
The star schema is preferred over a normalized schema because:
-	A star schema optimizes query performance and simplifies data retrieval in analytical environments (OLAP).
-	The star schema has a straightforward design with a central fact table and surrounding dimension tables, making it faster for read-heavy queries, such as aggregations and reports. 
-	Its denormalized structure reduces the number of joins required, leading to faster data processing, especially for large datasets. 
-	The star schema is easier for business users to understand and interact with, making it ideal for business intelligence and data warehousing.
-	 In contrast, a normalized schema is better suited for transactional systems (OLTP) where data integrity and minimizing redundancy are more important than fast query performance.

 
# Q2. What are the benefits of separating facts from dimensions?
Scalability:  
  - It enabled us to add new dimensions (e.g., dim_product) without altering fact tables.  
  - It also allowed us to expand fact tables with new metrics (e.g., quantity_sold).  

- Reusability:  
  - We noticed that dimensions like dim_time or dim_geography can link to multiple fact tables (sales, inventory).  

- Data Integrity:  
  - Dimensions enabled us to have consistent product IDs across all facts.  
  
  - Fact tables store numeric data in a compact format (ideal for aggregation).  




# Q3. What types of business decisions could this warehouse support?
 Sales & Marketing. 
 - The warehouse can assist in identifying high-value customers by region or purchase history.  Which is basically efficiency in customer segmentation.
  
  
- Optimization of inventory:  
  - The warehouse makes it easier to track stock levels and sales trends (join fact_sales with dim_products).  

 
- Revenue Forecasting:  
  - We also noticed that it can assist in efficiently predicting quarterly revenue using historical sales and dim_time.  


- Cost Reduction:  
  - The warehouse can also identify low-margin products via fact_sales and dim_products.  


