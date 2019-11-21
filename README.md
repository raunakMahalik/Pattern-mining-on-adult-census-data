# Pattern-mining-on-adult-census-data

## Introduction:
In this project I have captured the frequent patterns existing in the 'Adult census data'. To achieve this I have implemented 3 frequent pattern mining algorithms :

### i.) Apriori algorithm
### i.i) Improved Apriori with sampling
### ii.) FP- Growth algorithm

The above mentioned algorithms i.e. Apriori and FP-growth algorithms, are popular in finding frequent itemset patterns in transactional data. In this project along with implementing the Apriori and FP-Growth algorithms I have Implemented a variation of Apriori with sampling. This variation improves the speed of the algorithm while yielding similar results.

## About the data :
The Adult Census Data is an open source data available at the UCI website : https://archive.ics.uci.edu/ml/datasets/Adult . This data is cross sectional in nature and contains more than 30000 rows. The attributes present in the data are age, workclass, fnlwgt, education, education-num, marital-status, occupation, relationship, race, sex, capital-gain, capital-loss, hours-per-week and native-country. Most of the attributes are categorical in nature but there are 6 attributes which are continuous in nature (age, fnlwgt, education-num, capital-gain, capital-loss, hours-per-week).

## Data pre-processing:
Before subjecting the data to the pattern mining algorithms mentioned above, I cleaned the data to make it as close to a transactional data as possible. The adult census data set has some missing values represented by ‘?’, given that we have a lot of rows and only few missing values, I deleted the rows containing the missing values. After this I noticed that a few columns have continuous values. To apply frequent pattern mining algorithms the columns must have categorical data for we are interested in generating association rules from a limited pool of items appearing in the transactions. To achieve this, I have grouped continuous data into discrete bins (see table_1). This quantization was done on all the continuous variable columns except for the ‘fnlwgt’ and ‘education-num’ columns. I dropped these two columns entirely from my dataset as I believe these two columns do not provide any useful information.
