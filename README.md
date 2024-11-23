# Home Sales

**Dependencies**
1. findspark
2. pyspark.sq
3. pyspark

**Overview**

Via SparkSQL a machine is created based on the home sales data key metrics including dates, home prices, amount of bedrooms/bathrooms, the square feet of these rooms, number of floors and the view of the home which all play a role in the pricing of the home. Using spark the data is analyzed 
utilizing temporary views, partition data, cache and uncached temporary tables while comparing runtime of the various methods of sorting the data.

**Results**
The uncached runtime is 0.77 seconds while the cached runtime totals to 0.63 seconds which is 0.14 seconds less now that the data has been sorted through cache. On the other hand the cached runtime totals to 0.63 seconds while the parquet runtime totals to 0.89 seconds which is 0.26 seconds more now that the data has been sorted through parquet. This increase in time could be due to parquet splitting the data in a columnar format versus the cache data which is stored in fast access hardware that directly reduces the accessing storage layers and can in turn improve run time. 
