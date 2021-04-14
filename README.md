The Part 1 branch contains three different files. “Customer_segmentation” python code, “Customer Segmentation” tableau file and “Customer_segmentation_interpretation” excel file. 

The python script is the one that is executed first. It takes as input an extract of data from the table provided in BigQuery. Data manipulation tasks and statistical analysis are performed, and after examining the results, customers are assigned to segments. The final data frame with the assigned segments per customer is save as a csv file and is the data source used in tableau file. 

In the excel file there is a profiling of the different segments. 
Kindly note, that input data extract used in python is not attached in this public repository, in order to avoid any data privacy issues. Please let me know in case you need to share it with you.

As next step I would suggest that data acquisition is performed by using data directly from BigQuery with the use of API, or other available ways. In addition, the output data frame should be written from python to BigQuery and tableau can easily be connected there. This will ensure a smooth data flow. Unfortunately, I tried to write a table in BigQuery, but I didn’t have the required rights.

Below there is a description of the python code.

Data Acquisition 
•	Import Data from BigQuery to Python to perform the analysis. 
In this assignment data were imported through an extract from the BigQuery. 
Data Management
•	New columns are created for the revenue of every cuisine_parent
The initial data frame is in order_id level. Every row represents 1 row, so we have multiple rows for every customer.
•	The data frame is aggregated, so that the output will be in user_id (customer) level. Calculate sum/count of the respective columns as follows:
'order_id':'count'
'Basket':'sum'
'shop_id':'nunique' (count distinct)
'Breakfast_revenue':'sum'
'Healthy_revenue':'sum'
'Street_food_revenue':'sum'
'Italian_revenue':'sum'
'Creperie_revenue':'sum'
'Meat_revenue':'sum'
'Traditional_revenue':'sum'
'Ethnic_revenue':'sum'
'Sweets_revenue':'sum'
•	Column renaming for better understanding:
'order_id':'Num of Orders'
'Basket':'Revenue'
'shop_id':'Num of shops'
Analysis
•	Examine the statistics (min, max, mean, quartiles, etc) for the revenue & number of orders, as well as the distribution plots and boxplots.

New rows were added after going through the analysis results of the first version
Labelling & Segmentation
•	After examining the data and the charts/metrics mentioned above, we create two new columns with labels for categorizing users to S,M,L groups according to the number of orders and Revenue in January, as can be found below. 
Orders
S: 1, M:2-4, L: 5+
Revenue
S: 0-15€
M: 15-30€
L: 30€+
•	Examine metrics for every group combination of S,M,L Revenue & S,M,L Num of Orders (see excel file with the analysis)
•	Assigning Customers to segments
