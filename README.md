# Home_Sales

### Overview
In this project, I leverage SparkSQL to extract crucial metrics from a dataset of home sales. By employing Spark's functionalities, I generate temporary views, partition the data, and apply caching and uncaching operations on a temporary table. Additionally, I verify the successful removal of the table from the cache.

To accomplish this, I follow the following steps:

1. Utilizing SparkSQL, I create temporary views to enable SQL-like querying on the dataset.

2. I partition the data based on specific criteria, such as date or location, to enhance query performance and optimize data organization.

3. To improve query speed, I employ caching by storing the temporary table in memory, allowing for faster access in subsequent operations.

4. After completing the necessary operations on the temporary table, I uncache it to release the occupied memory and confirm its removal from the cache.

By employing Spark's capabilities, this project demonstrates how SparkSQL can be used to efficiently extract key metrics from home sales data. Through the creation of temporary views, partitioning, and caching operations, the project enhances data processing and facilitates effective data analysis.
