# Exploring Indian Census 2011 Data 

## Problem Statement
We have access to the Indian Census data for the year 2011 and the dataset is rich in information, but its sheer volume and complexity make it challenging to extract meaningful details without the aid of data science techniques.

By exploring this dataset, we aim to unravel essential demographic insights, highlighting the status of females in various roles within their households and communities. This data aids in policymaking, social development, and ensuring equitable opportunities for all.

## Methodology Used
The <b>first part </b> of this project includes the process of performing <b> Detailed Explanatory Analysis (EDA)</b> to draw meaningful conclusions with the help data visualisation techniques. 
The code for this part can be found in the file named [EDA_IndianCensus.ipynb](/EDA_IndianCensus.ipynb)

In the <b> second part, Principal Component Analysis (PCA)</b> is done on the given data by finding the components that show the most variance. This part is coded in the file [PCA_Indian Census_Shreya.ipynb](https://github.com/Shreya-Gupta1/PCA_Python/blob/main/PCA_Indian%20Census_Shreya.ipynb)

## Exploratory Data Analysis (EDA)

The various steps involved in performing the indepth explanatory analysis include- 

* To read the data and perform basic analysis that include-
  * check the shape and size of dataset
  * check the info for datatypes of columns.
  * check for null values and duplicates.

    After this preliminary analysis we can conclude that-
    * This census has 640 records and 61 variables.
    * There are no missing (null) values in the data.
    * Except for state and area name all the columns are of integer datatype.

* Next, with the help of seaborn library and other data visualization tools, we find answers to various questions like-
    1. How many districts does each state have?
    2. What is the Total population of India as well as male and female population distribution ?
    3. Analysis Of Literacy based on gender
    4. What is the distribution of non-working population as per gender and state?
    and many more

Further details and results drawn from this part of the analysis can be viewed [here](/EDA_IndianCensus.ipynb)

## Principal Component Analysis
In this project, we have chosen to treat outliers in the PCA analysis for the "PCA - Primary census abstract Dataset" which consists of 57 numeric columns. The decision to treat outliers is based on several reasons:
* Outliers can increase the error variance and reduce the power of statistical tests. If the outliers are non-randomly distributed, they can also violate the assumption of normality.
* Most machine learning algorithms, including PCA, may not perform well in the presence of outliers. Outliers can significantly impact the results and distort the principal components.
* Outliers have a disproportionate influence on the calculation of variances and covariances, which are crucial in PCA. By removing outliers, we can ensure that the principal components are not dominated by the extreme values.

Therefore, treating outliers in this case is necessary to obtain meaningful and accurate results from the PCA analysis.

Steps used for this analysis include- 
1. Scaling the method using z-score method. Box Plot before and after the scaling are also drawn for better understanding
2. Perform the Statistical Tests required before performing PCA. These include-
   * Bartletts test of sphericity
   * KMO Test
3. The results from these tests help us conclude that its necessary to perform the PCA. The next steps include-
   1. Create the covariance Matrix
   2. Get eigen values and eigen vector
   3. View Screen Plot to identify the number of components to be built
   4. Apply PCA for the number of decided components ot get the Loadings and compenet output

To view the code file for this part click [here](https://github.com/Shreya-Gupta1/PCA_Python/blob/main/PCA_Indian%20Census_Shreya.ipynb)

## Conclusion 

Few of the conclusions drawn from the data using the data visualization tools can be viewed here- 

![Slide1](https://github.com/Shreya-Gupta1/PCA_Python/assets/86680103/d3c960db-5fca-40fe-91c6-3259b453f017)

![Slide2](https://github.com/Shreya-Gupta1/PCA_Python/assets/86680103/99f7de07-ce3e-4e93-b5fe-78839b80ee53)

Conclusions drawn from the PCA Analysis are-
Observations:
* The first Principal component is positively correlated with Number of Household, Total Male & Female population, Literacy & Illiteracy Numbers among M & F, Number of SC in Males & Females, Working population, etc. These variables explain the most variance in the data i.e. 56%

* The Second Principal component is correlated with Marginal Cultivator Male/Female population and Marginal Agriculture (Male & Female) population etc. The Second PC explains about 14% of variation in the data.

* The Third Principal Component explains about 7% variation in the data. It positively correlates with Marginal Agriculture 0-3 Female, and 3-6 M&F Population.

* The Fourth Principal Component correlated positively with Marginal Households Male, Marginal Other (0- 3,3-6) Workers Male population. It explains about 6% of variation in the data.

* The Fifth Principal Component explains about 4% variation in data. It is positively correlated with Scheduled Tribes Population Male& Female, Non-working Male& Female population.

* The Sixth Principal Component explains about 3% variation in data. It is positively correlated with Female Marginal Other workers (0-3,3-6), Main & Marginal Households Female population.

Overall the first 6 PCs explain 90% variation in the data. Each PCs correlates with a different set of variables explaining how different aspects of population contribute to the variation in data.

