# anastasia_eksupno_fagito

This repository was created for the Head of Business Intelligence assignment.
It consists of three different branches one for every part of the assignment. 

The Part 1 branch contains three different files. “Customer_segmentation” python code, “Customer Segmentation” tableau file and “Customer_segmentation_interpretation” excel file. 
The python script is the one that is executed first. It takes as input an extract of data from the table provided in BigQuery. Data manipulation tasks and statistical analysis are performed, and after examining the results, customers are assigned to segments. The final data frame with the assigned segments per customer is save as a csv file and is the data source used in tableau file. 

In the excel file there is a profiling of the different segments. 
Kindly note, that input data extract used in python is not attached in this public repository, in order to avoid any data privacy issues. Please let me know in case you need to share it with you.

As next step I would suggest that data acquisition is performed by using data directly from BigQuery with the use of API, or other available ways. In addition, the output data frame should be written from python to BigQuery and tableau can easily be connected there. This will ensure a smooth data flow. Unfortunately, I tried to write a table in BigQuery, but I didn’t have the required rights.

In the branch Part-2 there is a pdf file with the development plans, as requested in the second part of the assignment. 

The branch Part 3 contains the 3 different scripts in SQL, Python & R. One can see the initial scripts provided and the update ones for every case, with commit messages with suggestions and comments after reviewing the scripts.
