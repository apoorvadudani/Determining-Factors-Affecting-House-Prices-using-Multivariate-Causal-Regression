# Determining-Factors-Affecting-House-Prices-using-Multivariate-Causal-Regression

## Background

Damian Realty is a fictional real estate company specializing in listings in upscale Hillsborough, California. I analyze their real estate data with the intent of understanding the variables that explain sales amounts. I collect a set of home sales detail data below (also found in the "Acme Realty dataset.csv" file in this repository). 

![image](https://user-images.githubusercontent.com/113878059/227744412-5ec7dc73-77de-4134-bed8-be8a7e37dde6.png)
 
The home sales detail data shows house characteristics of homes sold in Hillsborough, CA during the time period of 2008-2011, based on data from online real estate website Zillow. The home sales detail data includes the variables House, Price ($M), House (K sf), Lot (K sf), Bedrooms, and Bathrooms. The House column shows the house address for each house sold, with house numbers replacing actual house addresses for privacy reasons. Price ($M) shows the sales price for each house in millions of US dollars. House (K sf) shows the size of the interior of the house in thousands of square feet. Lot (K sf) shows the size of the building lot in thousands of square feet. Bedrooms shows the total number of bedrooms. Bathrooms shows the total number of bathrooms.

## Data analysis model selection and setup

I apply time-series and causal regression analysis techniques to conduct the analysis using Microsoft Excel, enhanced with the Analysis ToolPak (ATP) add-in.

I first forecast the price for a house size of 4000 sq. ft., a lot size of 22000 sq. ft., 4 bedrooms, and 5 bathrooms using time-series analysis. I define the price forecast equation relating Price, House Size, Lot Size, Bedrooms, and Bathrooms as follows: Intercept + (B18 * A25) + (B19 * B25) + (B20 * C25) +(B21 * D25)

I then build a multivariate causal regression to understand the variables that are important in determining sales prices, with the intent of forecasting prices for different types of houses. choosing this analysis method for the following reasons:

1. Degree of accuracy: 


I provide logical names for all variables and execute the regression analysis using a 95% confidence level.

## Findings

<img width="476" alt="image" src="https://user-images.githubusercontent.com/113878059/227742404-46c17bc3-ebc9-4d16-a0ad-1a63c6f0a9a2.png">

- Y-intercept value: -1.218314642
- X1 (House Size) coefficient: 0.36793450
- X2 (Lot Size) coefficient: 0.015595172
- X3 (Bedrooms) coefficient: 0.119113849
- X4 (Bathrooms) coefficient: 0.341296528
- Price forecast amount (found by plugging in the above values into the aforementioned formula): $2.78 million

## Interpreting results

In the multivariate causal regression, I observe that the coefficient for House Size (0.36) and number of bathrooms (0.34) is much larger than that for Lot Size (0.015). This means that house size and the number of bathrooms have the highest correlations with house prices. However, because the P-value is less than 5% for the number of bathrooms, I can assume that the proposed model has a statistically significant contribution and is not just the results of random data, and that leads to the number of bathrooms being the best indicator of house value

Based on the much larger coefficient value for number of bathrooms over Lot Size and number of bedrooms, as well as only the p-value for number of bathrooms being statistically significant, I thus infer that the number of bathrooms is the strongest factor in determining house prices, more so than even the house size.

## Literature review

According to Oikarinen & Hoesli (2008), additional bathrooms have a much higher value-added impact in higher-priced homes (like those in upscale Hillsborough, CA) than in lower-priced ones. This supports our finding.

## Stakeholder insights and actionable recommendations

I provide insights by interpreting the data to show what it means for the various business stakeholders involved, and provide recommendations on how to maximize house value for purposes of Amce Realty.

### Damian Realtors

![image](https://user-images.githubusercontent.com/113878059/227745044-5dd564eb-90f0-48fa-97fa-9ad9b02a7da4.png)

1.	Establish a strong brand identity that emphasizes luxury and exclusivity. Use high-quality marketing materials and focus on networking with high-end buyers and sellers.
2.	Use technology to reach a wider audience and showcase properties in innovative ways. This can include 3D virtual tours, social media advertising, and targeted email campaigns.
3.	Build relationships with realtors, building contractors, and government agencies to stay informed about market trends and regulations. This can help you to provide better service to your clients.

### Homeowners

![image](https://user-images.githubusercontent.com/113878059/227745063-1ae40fbc-8b91-4f2d-8aa9-d9ed4284554f.png)

1.	Adding an additional bathroom can significantly increase the value of a house, particularly in upscale neighborhoods like Hillsborough.
2.	Invest in high-end fixtures and finishes for the bathrooms. Consider features like heated floors, jetted tubs, and smart technology.
3.	Regular cleaning and maintenance can prevent damage and ensure that the bathrooms remain in top condition.

### Real Estate Agents

![image](https://user-images.githubusercontent.com/113878059/227745078-e25a5c05-9ea2-4603-b138-e94e39123406.png)

1.	Emphasize the number and quality of bathrooms in marketing materials and showings. Use professional photos to showcase the bathrooms in the best possible light.
2.	Stay informed about local market trends and preferences when it comes to bathroom features and styles. This can help you to provide expert advice to homeowners on how to maximize their house value.
3.	Suggest upgrades to homeowners that will increase the value of their bathrooms, such as adding high-end finishes or expanding the space.

### House Buyers

![image](https://user-images.githubusercontent.com/113878059/227745107-077cdbc9-6108-4091-be92-230c2b115298.png)

1.	Pay attention to the number of bathrooms when evaluating potential houses to buy. Houses with more bathrooms generally command higher prices, so consider this when making an offer.
2.	Look for houses with bathrooms that feature high-quality fixtures and finishes, such as granite countertops or high-end plumbing fixtures.
3.	Inspect the bathrooms carefully for any signs of damage or needed repairs. This can help you to negotiate a lower price or avoid costly repairs in the future.

### Building Contractors

![image](https://user-images.githubusercontent.com/113878059/227745155-2b9c1342-be8d-44af-ab13-9d3f61ad8f51.png)

1.	Focus on using high-quality materials and workmanship when building or renovating bathrooms. This can increase the value of the house and ensure customer satisfaction.
2.	Stay informed about the latest bathroom trends and preferences in the market. This can help you to offer innovative designs and features that will appeal to potential buyers.

### Building-Related Government Agencies

![image](https://user-images.githubusercontent.com/113878059/227745133-d6be4e30-0666-4c3d-84a5-3299304f8c6c.png)

1.	Offer incentives or tax breaks to homeowners who upgrade their bathrooms to more energy-efficient or high-quality features. This can promote sustainability and increase the value of the house.
2.	Set and enforce building standards that encourage the use of high-quality materials and workmanship when building or renovating bathrooms.

### House Sellers

![image](https://user-images.githubusercontent.com/113878059/227745146-18899cb3-e8bc-4b4d-a69a-e031a846d13b.png)

1.	Price the house appropriately based on the number and quality of bathrooms. Use market research and data to determine a fair and competitive price.
2.	Use professional photos and detailed descriptions to highlight the bathrooms in the house. Emphasize the number and quality of bathrooms in marketing materials and showings.

### Limitations of and recommended improvements to the data model

Because only one factor is statistically significant (number of bathrooms), additional internal variables, such as parking space size, number of in-built appliances, and number of storage units (such as closets), along with external variables, such as interest rates, could be analyzed to improve accuracy of the causal analysis results and help Damian Realty know what else affects house prices.

## References

Dataset obtained from: https://www.zillow.com/research/

Oikarinen, E., & Hoesli, M. (2008). Determinants of house prices: A quantile regression approach. Journal of European Real Estate Research, 1(3), 161-179. doi: 10.1108/17539260810926397

