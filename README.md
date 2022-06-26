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



