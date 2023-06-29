# Home_Sales

### Overview

In this project, I employ SparkSQL to analyze a dataset of home sales data and extract key metrics. The following steps outline the process:

1. Utilizing SparkSQL, I create temporary views that enable SQL-like querying on the dataset. I execute queries to answer specific questions, including:

   - Determining the average price for a four-bedroom house sold each year, rounded to two decimal places.
   - Calculating the average price of homes based on the year they were built, considering three bedrooms and three bathrooms, rounded to two decimal places.
   - Finding the average price of homes with three bedrooms, three bathrooms, two floors, and a minimum size of 2,000 square feet, rounded to two decimal places.
   - Assessing the "view" rating for homes with a cost of $350,000 or more and recording the query's runtime, rounded to two decimal places.

2. I partition the data based on the "date_built" field in the formatted Parquet home sales data. This step enhances data organization and query performance.

3. To improve query speed, I cache the temporary table containing the processed data. Additionally, I perform an uncaching operation to release the occupied memory and ensure removal from the cache.

4. By utilizing the cached data, I execute a query that filters out view ratings with an average price greater than or equal to $350,000. I measure the runtime of this query and compare it to the uncached runtime to assess the impact of caching.

5. I further optimize data processing by partitioning the formatted Parquet home sales data using the "date_built" field. I create a temporary table to store this data and execute a query filtering out view ratings with an average price greater than or equal to $350,000. Similar to the previous step, I measure the runtime and compare it to the uncached runtime, evaluating the effectiveness of partitioning and temporary table creation.

By employing Spark's capabilities, this project demonstrates how SparkSQL can be used to efficiently extract key metrics from home sales data. Through the creation of temporary views, partitioning, and caching operations, the project enhances data processing and facilitates effective data analysis.

### Result
The initial runtime recorded is 0.8110 seconds, followed by the second runtime of 0.6370 seconds after clearing the cache. Lastly, the third runtime achieved is 0.4646 seconds by utilizing partitioning in Parquet. Based on these observations, it can be concluded that partitioning Parquet yields the most effective method for enhancing data extraction efficiency.

#### 1st Run Time
![alt text](https://github.com/TaiShan16/Home_Sales/blob/main/Image/1st%20run%20time.JPG)

#### 2nd Run Time (after clearing cache)
![alt text](https://github.com/TaiShan16/Home_Sales/blob/main/Image/after%20cache%20runtim.JPG)

#### 3rd Run Time (partitioning Parquet)
![alt text](https://github.com/TaiShan16/Home_Sales/blob/main/Image/Partition%20run%20time.JPG)
