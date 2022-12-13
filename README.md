# Predictive Analysis of Housing Prices 

This project is part of the Big Data Analytics for Competitive Advantage (ITCS-6100) course from the University of North Carolina at Charlotte.

## Team Members:
- Vishwath Kamalanathan
- Udit Ghosh
- Swetha Natakala Ramakumar
- Shreya Sekhar
- Amruth Nag

## Communication Plan:
The team intends to communicate online on discord and will make time to meet personally on campus to work on the project whenever needed. 

## Business Opportunity and Domain Knowledge

### Business Problem/ Opportunity:

Buying a new property has always been a hustle. When people look out to buy a new house, they tend to be more conservative towards budget and market strategies. They attempt to optimize the budget to meet their requirements and needs. The perfect home meets and matches the customer's needs while staying within their budget. So, when it comes to budgeting, price prediction is crucial. People typically approach a real estate manager or an agent who predicts prices. It's beneficial but would raise costs because you must pay a commission to the manager. Instead, we are trying to build a model that helps to predict house prices by considering the prime features.

### Domain: 

Real-Estate, Sales, and Finance


### Domain Knowledge:

According to the California Census data released by the U.S. Census Bureau, each block group in California includes ten metrics, including population, proximity to the ocean, total room space, and bedroom details in the home. It aims to specify the project's functional and non-functional requirements and to serve as a resource for defining the project's scope.

Housing market is one of the most important indicators of economic development in a region. A strong housing market in a region signals strong economic growth. 


## Data

### Data Source:

Data - <https://www.dcc.fc.up.pt/~ltorgo/Regression/cal_housing.html>

AWS Sagemaker link - <https://catalog.us-east-1.prod.workshops.aws/workshops/80ba0ea5-7cf9-4b8c-9d3f-1cd988b6c071/en-US/2-real-estate>

<i>Note: We used latitude and logitutde to extract the county information and perfomed analysis at the county level. We also added in an extra feature which is used to get the population per room for each county. Link to the County Extraction notebook - [Extraction Notebook](Jupyter-Notebooks/County_extraction.ipynb)</i>

### Data Description:

|         Column Name         | Data Type |                                             Description                                             |
|:---------------------------:|:---------:|:---------------------------------------------------------------------------------------------------:|
| latitude                    | DECIMAL   | A measure of how far west a house is; a higher value is farther west                                |
| longitude                   | DECIMAL   | A measure of how far north a house is; a higher value is farther north                              |
| housing_median_age          | INT       | Median age of a house within a block; a lower number is a newer building                            |
| total_rooms                 | INT       | Total number of rooms within a block                                                                |
| total_bedrooms              | INT       | Total number of bedrooms within a block                                                             |
| population                  | DECIMAL   | Total number of people residing within a block                                                      |
| households                  | INT       | Total number of households, a group of people residing within a home unit, for a block              |
| median_income               | DECIMAL   | Median income for households within a block of houses (measured in tens of thousands of US Dollars) |
| median_house_value (target) | DECIMAL   | Median house value for households within a block (measured in US Dollars)                           |
| ocean_proximity             | STRING    | Location of the house w.r.t ocean/sea                                                                   |
| county                      | STRING    | County Based on the Latitude and Longitude                                                                |
| population/rooms                      | STRING    | Gives the ration of # people to # rooms in a county                                                 |


## Research Objectives and Question(s)

- Understand the distribution of the features through statistical analysis of the data
- Develop an understanding of the correlation between different features, and the target variable (i.e. Median House Value)
- Identify the locations which have the highest median prices historically using Geospatial Feature Engineering techniques.
- Generate insights on the ideal house price based on the population distribution
- Evaluate different regression models like XGBoost, Random Forest and Linear Regression to find the model that best fits the business requirements

## Exploratory Data Analysis And Interactive Dashboard

Link of the AWS Sagemaker Jupter Notebook:

https://grp7housing.notebook.us-east-1.sagemaker.aws/notebooks/grp7_housing.ipynb#

Link to the EDA Notebook - [EDA](Jupyter-Notebooks/grp7_housing.ipynb)

<i>Note: Data Preprocessing was also perfomed in the same Notebook along with EDA.</i>

Link to Tableau Dashboard:

https://public.tableau.com/app/profile/vishwath.kamalanathan/viz/ITCS-6100-Group7/Comparison#1

The Dashboard has two views, 
- Comparison: Provides the ability to compare Median House Price with other features like Mdeian House Age, Median Income and Population across different county
- EDA: This view provides interactive charts that helps us understad Median House Price distribution with respect to other features (Can be filtered for different counties) 

## Analytics, Machine Learning, Evaluation and Optimization

Link to the Notebook - [EDA](Jupyter-Notebooks/grp7_housing.ipynb)

<i>Note: Models are trained and optimized after the EDA section in the Notebook.</i>

Using the data and insights from the EDA we were able to build 5 different ML models (KNN, Linear Regression, XGBoost, Decision Trees, Random Forest Regressor) models to find which model gives us the best results. 

We were able to conclude that the XGBoost model outperformed every other model with a test accuracy of 75% and we performed Grid search CV to optimize the hyperparameters, which led to the increase in accuracy of 77%.

We also used AWS Sagemaker Canvas to train the model in an optimized fashion with accuracy of 78%.


## Results

We were able to predict the Median Home Income at a county level for the California Housing Market with an accuracy of 77%. The entire project was planned and executed using the CRISP-DM process. 


## Comments

- Data Cleaning: The dataset we have taken is the California housing dataset. By using Latitude and Longitude in the dataset, we identified the address and derived    county from it to understand where the house is located. The dataset contains null values, the null values are eliminated since it is negligible.
 
- Engineered variables: We used the latitude and longitude data to get the county level information and created another column that measures population per room at a county level. 

- Data Manupulation: For scaling the features, used minmaxscaler to scale the features. Use dummies for ocean proximity and county features.

- Future Work: We can use additional data points like GDP tied up with the county level information, this could be a very good indicator for the median house prices. Additionally, we could use complex optimization algorithms like Genetic Algorithms to find the optimal hyperparameters. 

### Instructions for Individuals that may want to use our work
  - Please refer to the readme to understadn the domain and the work 
  - All the work has been done using jupyter notebooks attached in the repository for reference










