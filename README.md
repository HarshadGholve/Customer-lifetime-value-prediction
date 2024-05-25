# **Customer Lifetime prediction value**

We invest in customers (acquisition costs, offline ads, promotions, discounts & etc.) to generate revenue and be profitable. Naturally, these actions make some customers super valuable in terms of lifetime value but there are always some customers who pull down the profitability. We need to identify these behavior patterns, segment customers and act accordingly. Calculating Lifetime Value is the easy part. First we need to select a time window. It can be anything like 3, 6, 12, 24 months. By the equation below, we can have Lifetime Value for each customer in that specific time window:

**Lifetime Value: Total Gross Revenue - Total Cost**

This equation now gives us the historical lifetime value. If we see some customers having very high negative lifetime value historically, it could be too late to take an action.

We are going to build a simple machine learning model that predicts our customers lifetime value.

Lifetime Value Prediction
Define an appropriate time frame for Customer Lifetime Value calculation
Identify the features we are going to use to predict future and create them
Calculate lifetime value (LTV) for training the machine learning model
Build and run the machine learning model
Check if the model is useful
1. How to decide the timeframe

Deciding the time frame really depends on your industry, business model, strategy and more. For some industries, 1 year is a very long period while for the others it is very short. In our example, we will go ahead with 6 months.

2. Identifying the features for prediction

RFM scores for each customer ID (which we calculated in the previous article) are the perfect candidates for feature set. To implement it correctly, we need to split our dataset. We will take 3 months of data, calculate RFM and use it for predicting next 6 months. So we need to create two dataframes first and append RFM scores to them.

After the first two steps, it is easy to calculate CLTV and train and test the model.

1. Identifying the features
2. Importing necessary libraries and packages and reading files
2.1 Feature Engineering
3. Recency
3.1 Assigning a recency score
3.2 Ordering clusters
4. Frequency
4.1 Frequency clusters
5. Revenue
5.1 Revenue clusters
6. Overall score based on RFM Clustering
7. Customer Lifetime Value
7.1 Feature engineering
8. Machine Learning Model for Customer Lifetime Value Prediction
9. Final Clusters for Customer Lifetime Value

# **About Dataset**
Abstract: A real online retail transaction data set of two years.

Data Set Information:
This Online Retail II data set contains all the transactions occurring for a UK-based and registered, non-store online retail between 01/12/2009 and 09/12/2011.The company mainly sells unique all-occasion gift-ware. Many customers of the company are wholesalers.

Attribute Information:

InvoiceNo: Invoice number. Nominal. A 6-digit integral number uniquely assigned to each transaction. If this code starts with the letter 'c', it indicates a cancellation.

StockCode: Product (item) code. Nominal. A 5-digit integral number uniquely assigned to each distinct product.

Description: Product (item) name. Nominal.

Quantity: The quantities of each product (item) per transaction. Numeric.

InvoiceDate: Invice date and time. Numeric. The day and time when a transaction was generated.

UnitPrice: Unit price. Numeric. Product price per unit in sterling (Â£).

CustomerID: Customer number. Nominal. A 5-digit integral number uniquely assigned to each customer.

Country: Country name. Nominal. The name of the country where a customer resides.

Link: https://www.kaggle.com/datasets/lakshmi25npathi/online-retail-dataset
