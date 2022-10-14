# Predictive Analysis of Housing Prices 

This project is part of the Big Data Analytics for Competitive Advantage (ITCS-6100) course from the University of North Carolina at Charlotte.

## Team Members:
- Vishwath Kamalanathan
- Udit Gosh
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
| ocean_proximity             | STRING    | Location of the house w.r.t ocean/sea                                                               |

## Research Objectives and Question(s)

- Understand the distribution of the features through statistical analysis of the data
- Develop an understanding of the correlation between different features, and the target variable (i.e. Median House Value)
- Identify the locations which have the highest median prices historically using Geospatial Feature Engineering techniques.
- Generate insights on the ideal house price based on the population distribution
- Evaluate different regression models like XGBoost, Random Forest and Linear Regression to find the model that best fits the business requirements






