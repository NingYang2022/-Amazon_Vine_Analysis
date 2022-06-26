# <font color=#6495ED>Amazon Vine Analysis</font>

## <font color=#6495ED>Project Overview</font>

Our project is analyzing Amazon reviews written by members of the paid Amazon Vine program. Amazon Vine invites the most trusted reviewers on Amazon to post opinions about products to help their fellow customers make informed purchase decisions. Vine program  allows manufacturers and publishers to receive reviews for their products. Companies pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

### <font color=#6495D>Purposes</font>

- Pick one of 50 datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. 

- Use PySpark to determine if there is any bias toward favorable reviews from Vine members in our dataset. 

## <font color=#6495ED>Resources</font>

### <font color=#6495D>Data Source: </font>

- Pick [furniture data file](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Furniture_v1_00.tsv.gz) from [50 Amazon Reviews Datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt)

### <font color=#6495D>Software:</font> 
- PySpark with Jupyter Notebook on [Google Colab](https://colab.research.google.com/?utm_source=scs-index)
- [Amazon S3 Storage](https://aws.amazon.com/s3/
)
- PostgreDB on [Amazon RDS](https://aws.amazon.com/s3/)
- PgAdmin 4

## <font color=#6495ED>Results</font>
- The PostgreDB tables on Amazon RDS had been populated with the data through the ETL process.
    1. review_id_table
![review_id_table](https://github.com/NingYang2022/Amazon_Vine_Analysis/blob/main/Images/review_id_table.png?raw=true)

    2. products_table
![review_id_table](https://github.com/NingYang2022/Amazon_Vine_Analysis/blob/main/Images/products_table.png?raw=true)

    3. customers_table
![customers_table](https://github.com/NingYang2022/Amazon_Vine_Analysis/blob/main/Images/customers_table.png?raw=true)

    4. vine_table
![vine_table](https://github.com/NingYang2022/Amazon_Vine_Analysis/blob/main/Images/vine_table.png?raw=true)

- There were **136** Vine reviews and **18019** non-Vine reviews.

- There were **74** Vine reviews that were 5 stars and **8482** non-Vine reviews were 5 stars

- **54.41%** of Vine reviews were 5 stars and **47.07%** of non-Vine reviews were 5 stars.


## <font color=#6495ED>Summary</font>

|  | All Reviews |  |
| :------:| :------: | :------: |
| Vine| 136 | 0.75% |
| Non Vine | 18,089 | 99.25% |
|Total|18,155||


|  | All Reviews |  |
| :------:| :------: | :------: |
|  5 Stars | 8,559 | 47.14% |
| All Others | 9,596 | 52.86% |
|Total|18,155||



|  | All Vine Reviews |  |
| :------:| :------: | :------: |
|  5 Stars | 74 | 54.41% |
| All Others | 62 | 45.59% |
|Total|136||


|  | All Non-Vine Reviews |  |
| :------:| :------: | :------: |
| 5 Stars| 8,482 | 47.07% |
| All Others | 9,537 | 52.93% |
|Total|18,019||

- Vine reviews account for only 0.75% of all reviews, which indicates that Vine program has little impact on results of star rating. This explains that **percentage 5-star reviews for total reviews(47.14%)** is similar to 
**percentage 5-star reviews for non-Vine reviews(47.07%)**

- There is a small positivity bias for reviews in the Vine program. Compared to non-Vine reviews**(47.07%)**, more than half of Vine reviews **(54.41%)** vote for 5 stars，which indicates that the Vine members tend to give 5 stars over non-Vine members. 

