# Neural Network Charity Analysis

## Overview:
The purpose of this is analysis is to use a neural network to predict whether applicants funded by Alphabet Soup would be successful if funded.  

The data file is a [CSV](https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/charity_data.csv) containing information on over 34,000 organizations.  This analysis is comprised of three broad steps.  The first step pre-processes the code.  The second step contains the first attempt of running the data through a neural network.  The third step employs various methods to optimize it.   The "IS_SUCCESSFUl" column is the target variable because the model is attempting to predict whether the organizations will be successful.  The remaining columns are features of the model.  

## Results:
* [Deliverable 1](https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/AlphabetSoupCharity.ipynb): Pre-Processing

Prior to running the data through the neural network, it needs to be processed.  Steps include dropping unnecessary fields, such as EIN and Name, and tabulating the unique values of each column.

![unique val](https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/resources/unique%20values.png)

Columns with unique values over 10 were binned.  The binned results replaced the original data frame prior to encoding it. 

![encode table](https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/resources/encode%20table.png)

* [Deliverable 2](https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/AlphabetSoupCharity.ipynb): Process Data Through the Model

The original model is comprised of 2 hidden layers with the first layer containing 80 neurons and the second layer containing 30 neurons.  The result of this model is not optimal since it only obtained a 72.7% accuracy rate and data loss of about 55.4%.

![first run](https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/resources/original%20results.png)

* [Deliverable 3](https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/AlphabetSoupCharity_Optimzation.ipynb): Optimize the Model

Various steps were completed in an attempt to optimize the results.  Additional processing of the underlying data included a decision to bin the "INCOME_AMT" column seemed because it has 9 unique values.  

![bin income 1](https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/resources/bin%20income%20amount%201.png)
The data was processed consistent with the steps described above, including the replacement of column values with binned values and encoding the columns.  Three attempts to optimize the model were made.  Unfortunately, all three attempts presented results similar to the attempt described above.

![3 results](https://github.com/laurlen2112/neural_network_charity_analysis/blob/main/resources/3%20results.png)

The first optimization attempt replaced the relu activation with tanH. The second attempt added additional layers to the model, and the third attempt additional neurons.  

 

## Summary:

Since the attempts described above have an accuracy rate of about 72%, these models are not desirable models to predict success.  As such, more work needs to be completed in order to use machine learning for prediction on this dataset.  It might be beneficial to conduct additional preprocessing of the data such as changing the bins and removing columns from the final analysis.  Also, a Random Forest Classifier (RFC) might be a good model to attempt because RFCs are scalable so they work on a large datasets, are less influenced by outliers, and work well when the dataset calls for binary classification.
