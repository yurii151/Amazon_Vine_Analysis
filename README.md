# Amazon_Vine_Analysis

## Overview of the Analysis

The purpose of this anlaysis is to read in data from Amazon and then, uploading that data into a database for analysis. In the first part of the project, I created a postgres SQL database from my Amazon RDS instance. Once the data was loaded in postgres and I confirmed the data, I closed the database instance on AWS. The second part of the project was to go through the data frames that were created.

## Results

The following results stem from the dataframe of all the reviewed items from the Amazon link, only including the items with helpful reviews:

<img width="665" alt="Screen Shot 2022-02-23 at 3 37 48 PM" src="https://user-images.githubusercontent.com/92888170/155427973-7dba20f5-18ee-4269-9d25-753775d3a97a.png">

Inorder to do the analysis, I had to seperate this dataframe into 2 dataframes, one with paid reviews (vine = Y) and unpaid revies (vine = N).

<img width="665" alt="Screen Shot 2022-02-23 at 3 39 42 PM" src="https://user-images.githubusercontent.com/92888170/155428971-34bbea74-b864-449c-ad36-6a9f4560879c.png">


<img width="665" alt="Screen Shot 2022-02-23 at 3 39 54 PM" src="https://user-images.githubusercontent.com/92888170/155429056-8906e2d7-f747-4cf2-a7e7-e9d054ae7709.png">

Once we get to this point, we can begin to answer some questions.

The first thing we want to know is how many of each type of review there is:

<img width="385" alt="Screen Shot 2022-02-23 at 3 42 00 PM" src="https://user-images.githubusercontent.com/92888170/155429368-8ca8d64b-0aff-48d2-b909-051cfd7b4cfe.png">

  - There were 94 paid reveiws and 40,471 unpaid reviews in the data set.

The next thing we want to know is how many of each typ of review were 5 stars. Then, using that data and the information from the first part, we can see what percentage of 5 stars reviews relate to the entire population:

<img width="676" alt="Screen Shot 2022-02-23 at 3 45 05 PM" src="https://user-images.githubusercontent.com/92888170/155429672-d2c53bc0-f076-45b0-9c94-d900cd6779b7.png">

  - There were 48 paid 5 star reveiws and 15,633 unpaid 5 star reviews in the data set.
  - 5 star reviews made up 51.06% of paid reviews
  - 5 star reviews made up 38.70% of unpaid reviews


## Summary

Based on the results, I would say there is a positive bias in terms of 5 stars being given more favorably to products in paid reviews compared with unpaid reviews. The sample size for the paid reviews is much smaller than the unpaid reviews, but there is enough of a discrepency to be a noticable difference. Another analysis I would perform to back up this statement would be to look at the helpful votes column, and see if there is any relationship between the amount of helpful votes and the star rating. 

