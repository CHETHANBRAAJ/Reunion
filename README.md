# Reunion
Data Assignment - Reunion

### Problem 1: Data Modelling (related to Problem 2)

Imagine you are designing a database for an e-commerce platform. The database should store information about products, customers, orders, etc. (this is only indicative; please feel free to create tables as per your imagination).

Customer details such as shipping address, contact number etc. can change over time. Each product can have multiple variants based on its attributes. Each variant may be launched at various times, then discontinued and then perhaps relaunched later as per the business requirements. Price of the product and its variants may keep on changing with time. We want to retain the historical information for these changes as well in our schema.

**You are required to:**

1. Design a **star-schema / snowflake schema model** for the above requirements
    1. Use an entity-relationship diagram (ERD) that represents the relationships between these entities
    2. Include the necessary attributes and primary/foreign key relationships. Briefly explain your design choices.
2. Generate and insert sample data in the above model. Include the process and code of generating random data in your submission. You data should have:
    1. At least 2 years of order history
    2. At least 10 products; at least 2 products with variants.
    3. At least 10 customers

### Problem 2: SQL (related to Problem 1)

With the above data, write SQL queries for the following:

1. Retrieve the top 5 customers who have made the highest average order amounts in the last 6 months. The average order amount should be calculated for each customer, and the result should be sorted in descending order.
2. Retrieve the list of customer whose order value is lower this year as compared to previous year
3. Create a table showing cumulative purchase by a particular customer. Show the breakup of cumulative purchases by product category
4. Retrieve the list of top 5 selling products. Further bifurcate the sales by product variants

### Problem 3: ETL

The below given json file contains data related to orchestra, theirs concerts, works, artists, etc. Since the data is in nested JSON format, its not possible to conduct any analysis on the raw data.

[nested_data](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/98b0fa4b-2a85-40e0-af20-5a2785c55c92/Untitled.json)

You are required to:

1. Load the data and perform transformations to simply the data and store it a normalized manner into smaller tables which are easier to analyze
2. Prepare an ERD of the normalized data tables showing relationships between the various entities
3. Implement the transformation using python (can use libraries) and SQL both and submit two separate solutions

### Problem 4: Streaming

Download and upload the below json files to a cloud storage (Azure, AWS, GCP) manually 

[json_files.zip](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7ea8decf-3497-46c4-8095-25ea0a81a40e/json_files.zip)

You are required to:

1. Ingest json files from the cloud storage using Apache Spark Structured Streaming or Databricks Autoloader (read the documentation if you are not familiar with these topics)
2. Write the ingested data to a table without any transformations
3. Infer the schema of the ingested data automatically instead of providing the schema manually
4. Auto-detection of new files in the cloud folder if more json files are added to it.

### Problem 5: Time Series

The excel below contains data on the work done by AGI bots who can multi-task and do multiple types of work. They record the start and end time of each task that they undertake along with the name of the activity in this excel file.

[Time Series](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a5d30693-0a11-417a-a01c-078ea10bea91/Untitled.xlsx)

Since the bots can multi-task and therefore can be doing multiple tasks in parallel, it is not possible to directly determine when they were working and when they were idle. You are required to:

1. Perform transformations on the data to output continuous periods (start, end) of work done by each bot and aggregate the activities done during such periods as an array against each period.
2. Solve the problem using python and SQL both
