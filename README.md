# Real Estate Exploratory Data Analysis
## Table of Contents
- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Tools](#tools)
- [Data Preparation and Cleaning](#data-preparation-and-cleaning)
- [Data Analysis](#data-analysis)
- [Results and Findings](#results-and-findings)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)

### Project Overview
This is an exploratory data analysis of real estate properties for sale in Southern California.

### Data Source
I obtained this data from Zillow through a webscarpping tool called "Property Search & Detail Tool" using an API from "Scrapeak". Then I saved it as a csv called 'socal_RealEstate.csv'.

### Tools 
- [Zillow](https://www.zillow.com/) - Collecting Data
- [Scrapeak](https://www.scrapeak.com/zillow-scraper/?ref=ariel) - API
- [Property Search & Detail Tool](https://propertysearch.streamlit.app/) - Webscrapping
- [Anaconda Navigator: Jupyter Notebook](https://www.anaconda.com/download) - Data Cleaning and EDA


### Data Preparation and Cleaning
I performed the following tasks to prepare and clean the data:
1. Initial analysis to understand the data.
2. Created a dataframe with only a subset of relevant features.
3. Checked for duplicates.
4. Identified and removed outliers.
5. Identified and removed columns with missing values.


### Data Analysis
I worked with features such as: 'latitude', 'longitude', 'price', 'bathrooms', 'bedrooms', 'livingArea', 'lotAreaValue'. 

Code example:
~~~python
socal_listings_clean.loc[(socal_listings_clean['bedrooms'] > 3)].sort_values('price').head(10)
~~~
### Results and Findings
The analysis results are summarized as follows:
1. Bedrooms and lot area value do not have a strong correlation with the price of the home as much as the other features such as bathrooms and living area. 
2. Therefore, it is possible to find a home with the most bedrooms for the best value.
3. I found 3 ideal homes to begin our home search.

### Recommendations
Based on the analysis, I recommend the following actions:
1. Start home search with the 3 properties found to be ideal homes.
2. Continue searching for homes with the most bedrooms for the best value, if needed.

### Limitations
1. Properties with 7 and 9 bedrooms were removed from the dataset as outliers.
2. The features 'datePriceChanged', 'priceReduction', 'priceChange' were removed due to having a significant number of missing values.

### References
1. Exploratory Data Analysis with Python Cookbook by Ayodele Oluleye
2. [Seaborn](https://seaborn.pydata.org/index.html)
