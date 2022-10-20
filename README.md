# Amazon_Vine_Analysis

## Overview
Our mission was a larger project: analyzing Amazon reviews written by members of the paid Amazon Vine program.

Background: The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews of their products. Companies like SellBy pay Amazon a small fee and offer products to Amazon Vine members, who then have to leave a review.
We need to select one of the datasets and run an ETL process using PySpark to extract the dataset, transform the data, connect to the AWS RDS instance, and load the transformed data into pgAdmin. Next, you'll use PySpark to see if your dataset is skewed toward positive reviews by Vine members. We then wrote a summary of the analysis for our supervisor, Jennifer, to present to SellBy stakeholders.


## Results
### ETL on the Amazon reviews
Using our knowledge of cloud ETL processes, we created an AWS RDS database with tables in pgAdmin, selected a dataset from the Amazon Review dataset, and extracted that dataset into a DataFrame. We also converted the DataFrame into four separate DataFrames that match the table schema in pgAdmin. We then upload the transformed data to the appropriate table and run a query in pgAdmin to confirm that the data has been uploaded.

![ETL on the Amazon reviews](https://github.com/Simro25011/Amazon_Vine_Analysis/blob/main/Resources/customers_table_sql.png)
![ETL on the Amazon reviews](https://github.com/Simro25011/Amazon_Vine_Analysis/blob/main/Resources/products_table_sql.png)
![ETL on the Amazon reviews](https://github.com/Simro25011/Amazon_Vine_Analysis/blob/main/Resources/review_id_table_sql.png)
![ETL on the Amazon reviews](https://github.com/Simro25011/Amazon_Vine_Analysis/blob/main/Resources/vine_table_sql.png)

### Determine Bias of Vine Reviews

We will determine whether reviews written as part of the Vine program are biased. For this analysis, we needed to determine whether paid Vine reviews affected the percentage of 5-star reviews.

- VINE REVIEWS ANALYSIS

![VINE REVIEWS ANALYSIS](https://github.com/Simro25011/Amazon_Vine_Analysis/blob/main/Resources/Vine_reviews_analysis.png)

- NON VINE REVIEWS ANALYSIS

![NON VINE REVIEWS ANALYSIS](https://github.com/Simro25011/Amazon_Vine_Analysis/blob/main/Resources/Non_vine_reviews_analysis.png)

## Summary
