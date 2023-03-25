# Determining-Factors-Affecting-House-Prices-using-Multivariate-Causal-Regression

## Background

Acme Realty is a real estate company specializing in listings in upscale Hillsborough, California. I analyze their real estate data with the intent of understanding the variables that explain sales amounts. I collect a set of home sales detail data below (also found in the "Acme Realty dataset.csv" file in this repository). 

![image](https://user-images.githubusercontent.com/113878059/227744412-5ec7dc73-77de-4134-bed8-be8a7e37dde6.png)
 
The home sales detail data shows house characteristics of homes sold in Hillsborough, CA during the time period of 2008-2011, based on data from online real estate website Zillow. The home sales detail data includes the variables House, Price ($M), House (K sf), Lot (K sf), Bedrooms, and Bathrooms. The House column shows the house address for each house sold, with house numbers replacing actual house addresses for privacy reasons. Price ($M) shows the sales price for each house in millions of US dollars. House (K sf) shows the size of the interior of the house in thousands of square feet. Lot (K sf) shows the size of the building lot in thousands of square feet. Bedrooms shows the total number of bedrooms. Bathrooms shows the total number of bathrooms.

## Data analysis model selection and setup

I first forecast the price for a house size of 4000 sq. ft., a lot size of 22000 sq. ft., 4 bedrooms, and 5 bathrooms using time-series analysis. I define the price forecast equation relating Price, House Size, Lot Size, Bedrooms, and Bathrooms as follows: Intercept+(B18*A25)+(B19*B25)+(B20*C25)+(B21*D25)

I build a multivariate causal regression to understand the variables that are important in determining sales prices, with the intent of forecasting prices for different types of houses, choosing this analysis method for the following reasons:

1. Degree of accuracy: 


I apply regression analysis techniques to conduct the analysis using Microsoft Excel, enhanced with the Analysis ToolPak (ATP) add-in. I provide logical names for all variables and execute the regression analysis using a 95% confidence level.

## Findings

<img width="476" alt="image" src="https://user-images.githubusercontent.com/113878059/227742404-46c17bc3-ebc9-4d16-a0ad-1a63c6f0a9a2.png">

Y-intercept value: -1.218314642
X1 (House Size) coefficient: 0.36793450
X2 (Lot Size) coefficient: 0.015595172
X3 (Bedrooms) coefficient: 0.119113849
X4 (Bathrooms) coefficient: 0.341296528
Price forecast (plugging in the above values into the aforementioned formula): $2.78 million

![image](https://user-images.githubusercontent.com/113878059/227744259-92dfdc2b-7f8d-4ca5-80a4-06d6b4fac272.png)

## Interpreting results



## Literature review



## Stakeholder insights and actionable recommendations

I provide insights by interpreting the data to show what it means for the various business stakeholders involved, and provide recommendations on how to maximize house value for purposes of Amce Realty.

Acme Realtors:
1.	Establish a strong brand identity that emphasizes luxury and exclusivity. Use high-quality marketing materials and focus on networking with high-end buyers and sellers.
2.	Use technology to reach a wider audience and showcase properties in innovative ways. This can include 3D virtual tours, social media advertising, and targeted email campaigns.
3.	Build relationships with realtors, building contractors, and government agencies to stay informed about market trends and regulations. This can help you to provide better service to your clients.

### Homeowners



1.	Adding an additional bathroom can significantly increase the value of a house, particularly in upscale neighborhoods like Hillsborough.
2.	Invest in high-end fixtures and finishes for the bathrooms. Consider features like heated floors, jetted tubs, and smart technology.
3.	Regular cleaning and maintenance can prevent damage and ensure that the bathrooms remain in top condition.

### Real Estate Agents

1.	Emphasize the number and quality of bathrooms in marketing materials and showings. Use professional photos to showcase the bathrooms in the best possible light.
2.	Stay informed about local market trends and preferences when it comes to bathroom features and styles. This can help you to provide expert advice to homeowners on how to maximize their house value.
3.	Suggest upgrades to homeowners that will increase the value of their bathrooms, such as adding high-end finishes or expanding the space.

### House Buyers

1.	Pay attention to the number of bathrooms when evaluating potential houses to buy. Houses with more bathrooms generally command higher prices, so consider this when making an offer.
2.	Look for houses with bathrooms that feature high-quality fixtures and finishes, such as granite countertops or high-end plumbing fixtures.
3.	Inspect the bathrooms carefully for any signs of damage or needed repairs. This can help you to negotiate a lower price or avoid costly repairs in the future.

### Building Contractors

1.	Focus on using high-quality materials and workmanship when building or renovating bathrooms. This can increase the value of the house and ensure customer satisfaction.
2.	Stay informed about the latest bathroom trends and preferences in the market. This can help you to offer innovative designs and features that will appeal to potential buyers.

### Building-Related Government Agencies

1.	Offer incentives or tax breaks to homeowners who upgrade their bathrooms to more energy-efficient or high-quality features. This can promote sustainability and increase the value of the house.
2.	Set and enforce building standards that encourage the use of high-quality materials and workmanship when building or renovating bathrooms.

### House Sellers

1.	Price the house appropriately based on the number and quality of bathrooms. Use market research and data to determine a fair and competitive price.
2.	Use professional photos and detailed descriptions to highlight the bathrooms in the house. Emphasize the number and quality of bathrooms in marketing materials and showings.

### Limitations of and recommended improvements to the data model

Because only one factor is statistically significant (number of bathrooms), additional internal variables, such as parking space size, number of in-built appliances, and number of storage units (such as closets), along with external variables, such as interest rates, could be analyzed to improve accuracy of the causal analysis results and help Acme know what else affects house prices.


