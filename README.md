*note: this is a project for DSCI 100 - a Data Science and Machine Learning course offered at UBC

# Predicting Vancouver house prices based on square footage #

## Introduction ##
The Vancouver housing market is notorious for its skyrocketing prices-- making it the "second-most unaffordable [housing] market" after Hong Kong (Bloomberg, 2019).

A newcomer to Vancouver looking for a home might wonder what prices are considered below market value when looking for homes. On the flip side, a seller might wonder whether they are pricing their home below, above, or at the market expectation in order to accelerate or decelerate their time-to-sale.

The price of a house can depend on a multitude of factors, including location, size, the age of the home, and many others. Based on information about the property, predictions can be made about the selling price of a home compared to others in the area.

The goal of our project is to utilize k-nearest neighbors regression analysis to determine the relationship between price and total square footage of houses in Vancouver. Our prediction is that the total square footage can be a good indicator of home prices in Vancouver. We will do this using a publicly available dataset from the website Kaggle,, which has price data, square footage, and other details about Vancouver houses from 2017-2020. This dataset was compiled by Darian Ghorbanian during his studies at UBC Sauder School of Business, pursuing his Master of Business Analytics.

Our Predictive Question is: “Does the square footage of a house in Vancouver have an impact on its selling price?”

## Methods and Results ##
We started by searching for and loading various datasets from the web to find useful, high quality, and non-biased sources of information; using the Kaggle API for seamless integration. Necessary data cleaning and transformations were performed to ensure data quality. We then split the dataset into training (75%) and testing (25%) sets. Subsequently, we employed a k-nearest neighbors regression model. To optimize the model's performance, we used cross-validation to determine the ideal value for 'k' (number of neighbors).

## Our Findings ##
Our analysis confirms a positive relationship between the square footage of a house and its selling price in the Vancouver housing market. The KNN regression model, while providing valuable insights, demonstrated that square footage alone cannot fully explain the considerable price variability observed in the dataset. Our cross-validation process identified an optimal 'k' value of 63, resulting in a Root Mean Squared Prediction Error (RMSPE) of approximately $437,251.  This indicates that while square footage influences price, a significant degree of unexplained variation remains. This suggests  that other factors, such as location, age of the home, amenities, and overall market conditions, play crucial roles in determining the final selling price of a house in Vancouver.

we can see below the fit of our model, and how it fails near the endpoints due to the lack of training area in those ranges.
![image](/visualization.png)




