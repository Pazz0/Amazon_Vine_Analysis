# Amazon_Vine_Analysis

## Overview 

In this project, we will analyze Amazon product reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review. We are going to determine if this program is appropriate for our client "SellBy".

We have access to approximately 50 datasets, each containing reviews of a specific product. We have chosen the Musical Instrument category as this has a healthy amount of Vine Reviews. First off we use PySpark to perform the ETL process to extract the large dataset, transform the data and connect to an AWS RDS instance. Then we load the transformed data into pgAdmin whoch we then export for analysis. Next, with our exported data we will use Pandas to determine if there is any bias toward favorable reviews from Vine members in our chosen dataset. We will do this by comparing reviews which are and are not in the Vine program.

## Results

### Total Reviews

* 2754 Vine reviews 
* 749845 non-Vine reviews

### 5 Star Reviews

* Vine reviews: 1741 5-star reviews 
* Non-Vine reviews: 442750 5-star reviews

### Percentage of 5-star Reviews

* 63.22% of Vine reviews were 5-star reviews.
* 59.05% of non-Vine reviews were 5-star reviews.

<img width="736" alt="Screen Shot 2023-04-06 at 10 01 35 AM" src="https://user-images.githubusercontent.com/18335464/230401416-ed540544-c004-4e3c-8904-7134a940daa8.png">

<img width="730" alt="Screen Shot 2023-04-06 at 10 01 48 AM" src="https://user-images.githubusercontent.com/18335464/230401214-8ba53d20-403e-4361-91a9-b4d2edc3099c.png">

## Summary

Based on the analysis performed, it appears that there is a slight positivity bias for reviews in the Vine program. A higher percentage of Vine reviews were 5-star reviews compared to non-Vine reviews. This may be due to the fact that Vine reviewers are incentivized to write positive reviews. 

### Future Analysis
One additional analysis that could support this statement would be to analyze the text of the reviews using ML to see if there is any difference in the language used between Vine and non-Vine reviews. This could provide further insight into whether or not there is a bias towards Vine reviews.
