# Exploring Indian Census 2011 Data 

## Problem Statement
We have access to the Indian Census data for the year 2011 and the dataset is rich in information, but its sheer volume and complexity make it challenging to extract meaningful details without the aid of data science techniques.

By exploring this dataset, we aim to unravel essential demographic insights, highlighting the status of females in various roles within their households and communities. This data aids in policymaking, social development, and ensuring equitable opportunities for all.

# Methodology Used
The first part of this project includes the process of performing Detailed Explanatory Analysis (EDA) to draw meaningful conclusions with the help data visualisation techniques. 
The code for this part can be found in the file named- "EDA_IndianCensus.ipynb"

In the second part, Principal Component Analysis (PCA) is done on the given data by finding the components that show the most variance. This part is coded in the file- "PCA_IndianCensus.ipynb"

# Exploratory Data Analysis (EDA)

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
