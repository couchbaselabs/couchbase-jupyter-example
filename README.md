# couchbase-jupyter-example

## Summary

This repository includes an example Jupyter notebook that walks through how to access data stored in a Couchbase cluster from the Jupyter Notebook environment.

We will get the data from the Couchbase cluster and use it to train a linear regression model. The goal is to take a particular sample and predict the value of a target variable using different categorical variables using a linear regression equation.

Data set used is the [Advertising Dataset](https://www.kaggle.com/ashydv/advertising-dataset/version/1) from Kaggle.

## How to Run

- Install requirements.

  `$ pip install -r requirements.txt`

- Load the Dataset in the Couchbase Cluster using [`cbimport`](https://docs.couchbase.com/server/current/tools/cbimport.html) or using the Admin Console as described in the accompanying blog post.

- Open the Notebook and adjust the username and password in the first cell to reflect the password used for your cluster. Also adjust the Cluster connection string, bucket and collection settings if they are different from the ones in the Notebook.

  `pa = PasswordAuthenticator("Administrator", "123456")`

  `cluster = Cluster("couchbase://127.0.0.1", ClusterOptions(pa))`

  `bucket = cluster.bucket("TestBucket")`

  `collection = bucket.default_collection()`

- The code in the Notebook should now run without issues.
