
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

- Sevidzem Marilyn (@marilynmaika)
- Hetal Kumbharana (@HetalK4)
- Chad Mutinda (@Chad-Mutinda)
- Mangu Rita (@ritzy10)


## License

MIT License
<<<<<<< HEAD
=======

# Part 5: Reflection & Discussion
Discussion Questions:
# Q1 Why use a star schema instead of a normalized schema?

 
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
 - The warehouse can assist in Identifying high-value customers by region or purchase history.  Which is basically efficiency in customer segmentation.
  
  
- Optimization of inventory:  
  - The warehouse makes it easier to track stock levels and sales trends (join fact_sales with dim_products).  

 
- Revenue Forecasting:  
  -We also noticed that it can assist in efficiently predicting quarterly revenue using historical sales and dim_time.  


- Cost Reduction:  
  - The warehouse can also Identify low-margin products via fact_sales and dim_products.  


