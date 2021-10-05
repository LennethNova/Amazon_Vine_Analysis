# Amazon_Vine_Analysis

## Overview of the analysis
The Purpose of this analysis is to perform an ETL process to extract a dataset, transform the data, connect to an Amazon Web Services RDS instance and load that transformed data into PgAdmin. After that process, it is needed to determine id there is any bias toward favorable reviews from Vine members.

## Results:
There is a total of 4,291 vine member reviews while there is 1,781,706 non vine members. This is considering only vine or non vine members as filters.

![Vine](https://github.com/LennethNova/Amazon_Vine_Analysis/blob/main/images/c16.PNG)

![nonVine](https://github.com/LennethNova/Amazon_Vine_Analysis/blob/main/images/c17.PNG)

Considering the filters to retrieve all the rows with the total votes count equal or greater than 20 and filtering the data again in order to get all the rows where the helpful votes are divided by the total votes in the respective columns that are equal or greater than 50%. There were a total of 94 votes that were paid and only 48 of those votes were 5 stars making it only 51.06%, again, the total was obtained considering the previously filters mentioned above. The total votes of the unpaid ones is 40,471, but only 15,663 of the total voted for a 5 star, making 38.70% of the unpaid votes.

![Data01](https://github.com/LennethNova/Amazon_Vine_Analysis/blob/main/images/c14.PNG)

![Data02](https://github.com/LennethNova/Amazon_Vine_Analysis/blob/main/images/c15.PNG)

Adding another filter to the data, in order to verify the purchase of the product, it shows that non of the vine members purchased the products and gave a 5 star, while 3,862 of 10,106 unpaid ones gave a 5 star rate covering a 38.21% of the verified purchase 5 star rate for the unpaid members.

![AdditionalFilter](https://github.com/LennethNova/Amazon_Vine_Analysis/blob/main/images/c20.PNG)

## Summary:
There doesn't seem to be any positivity bias for the reviews in the vine program, specially from the paid votes with verified purchase. And even if considering the unverified purchase, it might be a lot 51.06% but at the same time, that considers low voters count in comparison with the non paid members. This last filter that was used to see the difference as accurate as possible,is one of many that could be use in order to give more meaning to the data. Also there are different ways to get to these results and at the same time there could be an analysis that could allow us to see the best selling and the best evaluated videogames and videogame related products.

###### Data from: *https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt*, *https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Video_Games_v1_00.tsv.gz*
