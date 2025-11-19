# Cafe sales database setup
This project simulates the role of a data engineer in designing and setting up a analytics-ready database for a cafe. '
The raw dataset comes from `ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training`, provided as `dirty_cafe_sales.csv`.\
The main workflow is implemented in `1_database_setup.ipynb` and is divided into 3 major parts.

##### 1. Data Exploration
This section performs initial interaction with the raw data using `kaggle API` and `PySpark`:
* Load the raw dataset and inspect its basic characteristics.
* Clean inconsistent values, ensure proper data types and rename columns for usability.

##### 2. Creating Database with Star Schema
This section focuses on `database design` using a `Star Schema`:
* Design fact and dimension tables for the cafe sales data.
* Use `psycopg2` to connect to a local `PostgreSQL` and execute `1_databae_setup.sql` to create the Fact and Dimension tables with proper constraints.
* Use `PySpark` to transform and clean dataset into Fact and Dimension table dataframes 
* Export these dataframes to csv file for further loading to the database.

##### 3. Simple Exploratory Analysis on Aggregated Data
This section include the using `PySpark Aggregation Method` to answer business questions including:
1. Total income across all transactions
2. Total quantity sold per item
3. Number of transactions by payment method
4. Top 3 best-selling items (quantity-based) for dine-in transactions 
5. Number of transactions per month
6. Month with the highest total income

Visualizations including:
1. Bar chart showing total revenue per item
2. Pie chart showing the distribution of payment methods
3. Line chart showing total monthly sales
4. Stacked bar chart showing sales per item broken down by location type
5. Box plot of Total Item Price grouped by item

## Contact
Settawuth Rattanaudom