# ist1314-chunkz
IST3134 Big Data Analytics
Comparing Apache Spark vs Pandas on the Olist e-commerce dataset 
This project investigates what drives negative customer reviews on an 
e-commerce marketplace by analysing delivery delay and review patterns 
per product category, and compares a distributed Apache Spark implementation 
against a single-machine Pandas implementation in terms of performance, 
scalability, and code complexity.

## Dataset
Brazilian E-Commerce Public Dataset by Olist (Kaggle):
https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

Only four datasets were required for this analysis: 
under `data/`:
| Dataset | Purpose |
|---|---|
| olist_orders_dataset.csv | Contains order timestamps and delivery information |
| olist_order_items_dataset.csv | Links orders with purchased products |
| olist_products_dataset.csv | Provides product category information |
| olist_order_reviews_dataset.csv | Provides customer review scores |

## How to Run

### Pandas (Google Colab)
1. Open `scripts/pandas_pipeline_colab.ipynb` in Google Colab
2. Run the setup cell, then run the upload cell — this opens a **Choose Files** 
   button; manually upload the 4 CSVs from `data/` in this repo (or your own 
   local copies) when prompted
3. Run the remaining cells in order
   
### Spark 
1. Open `scripts/spark_pipeline_glue.ipynb` in AWS Glue Notebook.
2. Upload the dataset files into your Amazon S3 bucket and update the S3 path inside the notebook.
3. Run all cells in order. The notebook will execute the Spark pipeline, including data cleaning, joining, aggregation, and machine learning.

