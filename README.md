# Multiple Linear Regression 

# Description

For this project, I examined an well-known and open-source dataset: King County House Sales.  The dataset included information around residential home sales for King County, Washington from May 2014 - May 2015.  The objective was to obtain, clean, explore, and model the dataset with a multivariate linear regression to predict the sale price of houses as accurately as possible as well as investigate what features postively and negatively effect price.  

The initial dataset included 21 columns with various data types representing home and lot size, bedroom and bathroom counts, the age and condition of the home, as well as geographic data.

Various forms of exploratory data analysis (eda) were to examine each feature for datatype, missing values, distributions, outliers, and preliminary correlations.  This process informed how to best clean data and assign categories appropriately to retain as much data as possible, while removing that which could impede an accurate model creation.   

Outliers were removed using [z-scores](https://www.statisticshowto.com/probability-and-statistics/z-score/) and those features that most highly correlated were evaluated to drop several columns that either provided very little insight (eg, id provides no value).  The data was then normalized and scaled accordingly.  

An initial model was created via [statsmodels api](https://www.statsmodels.org/stable/index.html) and evaluated with a qq plot.  


The initial model performed poorly.  By removing outliers from the target, the model improved and it was discovered (not shockingly) that 79% of the price was effected by 
* location - this was demonstrated by zip code
* size - square feet of living space
* grade - the quality of materials and construction used in building the structure

as the top three factors and each had a postive impact.  

The condition or how recently the house was built or remodeled came in next as well as the number of bathrooms - the more bathrooms, the higher the price.

1) zipcode 98003 and others (see below)

2) sqft_living_log coef = 2.218e+05 (log value) adjusted coef = 221 Price increases by 221 each sqft

3) grade coef = 7.344e+04

4) condition coef = 1.956e+04

5) bathrooms coef = 1.7e+04





## Main Files

student.ipynb - Notebook inclues data, methodologies and modeling around predictive model

K_C_RealEstateEval_2014_2015.pdf - presentation summarizing findings for a non-technical audience

## Additional Files

### Blog Post: [Categorical Data](https://andiosika.github.io/categorical_data)

### Video Presentation for Non-Technical Audience: [King County Residential Real Estate Evaluation 2014-2015](https://github.com/andiosika/Multivariate-linear-regression-for-predicting-home-prices/blob/master/zoom_0.mp4)
