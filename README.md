# Home_Sales
Module 22
Performance Results Summary

Uncached Query on CSV Data:

Runtime: Approximately 3.32 seconds. This is the time taken to execute the SQL query on the home_sales DataFrame, which is not cached.

Cached Query on CSV Data:

Runtime: Approximately 1.31 seconds. This shows a significant improvement due to caching, which allows Spark to use the in-memory data instead of reading from disk.

Query on Parquet Data:

Runtime: Approximately 0.61 seconds. This query is executed on the partitioned_home_sales DataFrame, which is stored in Parquet format.

Analysis

Comparison of Performance: The runtime for the query on Parquet data (0.61 seconds) is faster than both the uncached query (3.32 seconds) and the cached query on the CSV data (1.31 seconds). This indicates that Parquet format provides better performance than both uncached and cached CSV data for this specific query.

Conclusion

Parquet Performance: The Parquet data format performed better than the cached CSV data in this scenario. This is likely due to the optimized storage structure of Parquet, which allows for faster read times and better compression.
