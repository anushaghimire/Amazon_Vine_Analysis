# Amazon_Vine_Analysis
# Overview
## About
### Data source : https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Wireless_v1_00.tsv.gz
### Languages Used:
- PySpark
- Jupyter notebook
- pgAdmin 4
- AWS
- PostgreSQL
-  Google Colab Notebook
-  pandas



## Purpose: 

The purpose of the study is to analyze Amazon reviews written by members of the paid Amazon Vine program and to determine if there is any bias toward favorable reviews from Vine members in the dataset. To do the project I picked one dataset from  https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt and used PySpark to perform the ETL process. I extracted the dataset as dataframe and then transformed the dataset into 4 different dataframes: customers_table, products_table, review_id_table, and vine _table. Then I loaded the transformed data into pgAdmin and ran query to check tables have been populated correctly.

To determine the bias of vine reviews I used pandas to read the vine_table dataframe, then filtered data to calculate the percentages of vine 5-star reviews vs non-vine 5-star reviews.
## Results

- How many Vine reviews and non-Vine reviews were there?

**Vine reviews:**  There were 613 vine reviews.
                  
                  
<img width="556" alt="Screen Shot 2021-10-14 at 10 37 08 AM" src="https://user-images.githubusercontent.com/85364095/137398859-fad0c7d0-8bbe-4636-89d7-aa354502f7a0.png">

**Non-Vine reviews:**  There were 64,968 non-vine reviews.

<img width="556" alt="Screen Shot 2021-10-14 at 10 37 23 AM" src="https://user-images.githubusercontent.com/85364095/137398842-ad64c67e-41bc-4fae-a794-46bea05d6553.png">


- How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

**There were 200 5-star vine reviews.**

<img width="556" alt="Screen Shot 2021-10-14 at 10 37 42 AM" src="https://user-images.githubusercontent.com/85364095/137398782-6e5b791f-0897-4424-b6d3-52436ea50412.png">

**There were 28,842 5-star non-vine reviews.**

<img width="556" alt="Screen Shot 2021-10-14 at 10 37 55 AM" src="https://user-images.githubusercontent.com/85364095/137399299-bd860c0a-3bb5-47e3-9366-d729d1ebcf20.png">



- What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

**There were 32.6% paid 5-star reviews.**

<img width="556" alt="Screen Shot 2021-10-14 at 10 38 17 AM" src="https://user-images.githubusercontent.com/85364095/137369497-97123f16-4dce-4326-b8ee-4e3bd6ce7378.png">


**There were 44.3% unpaid 5-star reviews.**

<img width="556" alt="Screen Shot 2021-10-14 at 10 38 39 AM" src="https://user-images.githubusercontent.com/85364095/137369506-ae3c901d-f8f5-41c3-9d7d-70b10f6cd81b.png">



## Summary
Based on the results shown above there were no biased 5-star ratings by the paid reviewers for the product. Only 32.6% of the paid reviews were 5 stars whereas 44.3% 5-star rating was from unpaid reviews.



