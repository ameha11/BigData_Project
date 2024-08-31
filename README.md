# Customer Segmentation Analysis Using PySpark

## Project Overview
The Business-to-Consumer online retail sector is inherently competitive, with companies heavily investing in acquiring new customers while prioritizing customer loyalty and profitability to grow market share.

One of the most effective ways to retain customers is by identifying potential churn early and acting quickly to prevent it. Detecting early signs of churn, understanding customer needs based on their behavior, and automating personalized win-back campaigns are essential strategies for sustaining business in today’s competitive landscape (Neslin et al., 2006).

## Project Objective
This project aims to analyze the likelihood of customer attrition in the online retail market using RFM (Recency, Frequency, Monetary) analysis. RFM is a proven marketing model for customer segmentation based on transaction history—how recently, how often, and how much a customer has spent.

By assigning scores to each customer, this analysis helps predict those at risk of churning, while also exploring various related questions.

- Who are the best customers?
- Which of your customers can be retained?
- Who are the loyal customers?
- Where are our new customers?
  
This project explores which customers are truly at risk to churn and it provides insights on which target incentives would be useful for customers to stay and extend the customer’s lifetime value (CLV) in the online retail market.

## Business Understanding
Retaining customers is one of the most critical challenges in the online retail market. Hence, using customer transaction data to investigate the likelihood of a customer leaving the online retail market to understand their customer churn is crucial to extend their customer’s lifetime value (CLV) and identify loyal customers.

## Data Mining
The data set for this project “Online Retail Data Set” is retrieved in a csv format from the “UCI Machine Learning Repository”. The UCI Machine Learning Repository is a collection of databases, domain theories, and data generators that are used by the machine learning community for the empirical analysis of machine learning algorithms. Since 1987, it has been widely used by students, educators, and researchers all over the world as a primary source of machine learning data sets. As an indication of the impact of the archive, it has been cited over 1000 times, making it one of the top 100 most cited "papers" in all of computer science.

### Attribute Information:
- InvoiceNo: The Invoice number is a 6-digit integral number uniquely assigned to each transaction. If this code starts with the letter 'c', it indicates a cancellation. It is a string data type.
- StockCode: This is the product (item) code. It is a 5-digit integral number uniquely assigned to each distinct product.
- Description: Product (item) name. It is a string data type.
- Quantity: The quantities of each product (item) per transaction. It is a numeric data type.
- InvoiceDate: The day and time when a transaction was generated. It is a datetime data type.
- UnitPrice: This is the product price per unit in Euros(€). It is a numeric data type. It is a string data type.
- CustomerID: This is a 5-digit integral number uniquely assigned to each customer.
- Country: Country name. Nominal. The name of the country where a customer resides.

## Data Cleaning
As a next step, this project will evaluate the missing values within the data set to better understand how to deal with them. First, we search for patterns within the variables through visual inspection. There, we speculate how the distribution of the missing values would look like if they were available by discussing if the missing data is “missing completely at random”, “missing at random” or “not missing at random.” Also data types are checked, to ensure that accuracy in the analysis. Before doing the analysis and prediction, the data is checked if it is normalized. Furthermore, it is ensured that all column names are well described. Some of the country names that are not understandable such as 'ERIE' into 'Ireland'. Dropped rows that contained Missing Customer ID,Missing Stock Description, Abnormal Stock Codes that did not conform to the expected format, such as Stock Codes that started with letters, and had less than 5 digits. 

## Data Exploration
From the data set we explore basic questions to have a better understanding of the data. For example, what are the most returned products? What are the countries with the lowest sales volume? How many times did a transaction occurred in a country? What are the sales of each country except UK? In some instances like the previous question, the UK is excluded as, the online retail market is based in the UK and it has the largest distribution, hence for proper deep dive analysis of other regions it has been excluded as it skews the data. Other questions like what are the quantity of products sold in all the countries except the UK? are also explored.

## Feature Engineering
The following new feautures are included in the data set for better prediction:

- Recency: How 'recently' has a customer made a purchase. The lower the value the better based on a 1-5 rank.
- Frequency: How often does a customer purchase. The higher the value the better, based on a 1-5 rank.
- Monetary Value: How much money does a customer spend. The higher the value the better, based on a 1-5 rank.
- RFM Score: It is a combination of the individual R, F, and M rankings to arrive to a RFM score.

## Segmentation and Clustering
- At this stage, we segment our customers using RFM analysis to gain insights into their behavior.

## Predictive Modelling
- K-means is an unsupervised machine learning algorithm, which is used for data clustering. In k-means algorithm number of clusters K is predetermined and the algorithm iteratively assigns each data point to one of the K clusters based on the feature similarity.
- Implementation of K Means Clustering
    - Preprocessing the Data
    - Determine the Number of Clusters
    - Running K Means Clustering on the Preprocessed Data
    - Analyse the clusters
 
## Data Visualization
- The segments derived from the RFM Analysis and RFM is visualized on a bar chart in the jupyter notebook.
- Finally, the front-end of this project consists of a dynamic Power BI dashboard generated from the RFM and  visualizes the results in dashboard.

## Tools and Libraries used for the Project
- numpy 
- pandas
- matplotlib
- seaborn
- pyspark



