# Predictions_of_Sales
Goal: Predicting and improving sales of grocery and supermarket products with different variables. 
Methods: Data Visualizations and Machine Learning (Decision Trees and Linear Regression)

During this project, I cleaned the data, created and analyzed the data with visualizations, and created machine learning techniques to evaluate and create models for predicting the data. 

I conclude the project with a slides presentation to show my overall findings and make suggestions for how to use this data for predicting and improving sales for this market, which is all included in this README.

# Data Visualizations:

![correlations sales](https://user-images.githubusercontent.com/86759538/131196927-349517a4-f84c-46b2-ab83-d017e79d637d.png)

Heat map of numerical relationships within the data set. There is a moderate correlation between Item_MRP (maximum retail price) and Item_Outlet_Sales (total sales for an item at outlet).

## Grocery Stores vs. Supermarkets
![supermarket vs grocery numbers](https://user-images.githubusercontent.com/86759538/131197038-6459b98c-16cb-496f-af1c-62fde6cbadc8.png)

There are significantly more supermarkets in our data set than grocery stores. This can skew our data if not separated.

## Grocery Store Sales:
![grocery store sales](https://user-images.githubusercontent.com/86759538/131197012-fffa0955-74c0-4dff-b80b-0c2bd5ac66c7.png)

At a lower scale, but the sales are skewed to the right; more items are sold at a lower sales yield.

## Supermarket Sales:
![total sales supermarket](https://user-images.githubusercontent.com/86759538/131197141-90e81579-98d5-48d5-9f04-ad9714aeeb80.png)

Higher scale than grocery stores, sales are also skweed to the right; more items are sold at a lower sales yield as well.

## Types of Items:
![type of item](https://user-images.githubusercontent.com/86759538/131197189-4c5c7cdc-a9e0-437b-81c3-fe386fa5a877.png)

Different categories for items in general are proportional, between lower outlet sales and higher, however, for seafood it is proportionally more similar between the lower and higher brackets, indicating that category performs better for their sales.

## Categorical Features:
![features](https://user-images.githubusercontent.com/86759538/131197290-c57b6173-eaab-4194-9309-0f0b3f665723.PNG)

Similar to a heatmap, this bar chart measures the importance of different features on our target, the Item_Outlet_Sales. The features that most impact our sales are 25 and 24: which is what type of outlet it is, a grocery store or a supermarket. This seems to indicate that our supermarkets will sell a particular item better than a grocery store would.

Features 0, 17, 9, 21, 22, and 23 are at a much less magnitude, but still noticeable compared to the others. Negatively impactful are the item visibility and dairy. This would indicate that visibility scores can definitely negatively impact your item. Dairy, however, is an interesting find. We can make assumptions as to why dairy does not sell as well, but it could relate to competition, expiration dates/waste, or even different kinds of milk. 
Feature 17 is Seafood. This indicates that seafood yields high sales.
Features 21, 22, and 23 are the three tiers of the outlet locations. We do not have a definition for what these relate to, however, we can see that Tier_Type_1s perform poorly, in fact, negatively affecting sales, while tier_2 and tier_3 perform better. Tier_2 performing the best.

# Machine Learning
I performed Linear Regression, Simple Trees, Bagged Trees, and Random Forest models to see which may be best for predicting our Item_Outlet_sales.

## Bagged Trees: 
* R2 score 
  * Train: 0.9393579272736498
  * Test: 0.55099315926325
* RMSE 
  * Train: 423.6360797480683 
  * Test: 1113.0137805357635

## Random Forests :
* R2 score 
  * Train: 0.6104682601982897
  * Test: 0.6026003233209926
* RMSE  
  * Train: 1073.6861410348588
  * Test: 1047.0991749300013
  
## Linear Regression:
* R2 score
  * Train: 0.5264424685603024
  * Test: 0.5183542888366527
* RMSE 
  * Train: 1183.838053891126
  * Test: 1152.7573803143312

## Simple Tree:
* R2  score 
  * Train: 0.6039254897160836
  * Test: 0.6039254897160836
* RMSE 
  * Train: 1082.6656773340972
  * Test: 1057.3947626960721

Comparing the R2 scores and RMSE, I conclude the best model to use for this dataset is the Random Forests. I chose this because the R2 scores are comparable and highest for testing, while also having the lowest RMSE.

# Recommendations
My conclusions and suggestions would be as follows:
* Focus on supermarkets vs. groceries
* Proper visibility of items
* Competitive prices for items and/or periodic sales
* Focus on Tier 2 Outlets 
  * Avoid Tier 1
* Seafood is a profitable market 
  * Dairy less so
