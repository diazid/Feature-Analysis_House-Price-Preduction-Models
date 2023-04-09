# Home Values: Belt-Exam-A

by Israel Diaz

---

### Part 1

#### Explain the Linear Regression Model

![png](/img/lr_coefficientes.png)

**Top 3 Positive Coefficients**

* Central Air_Y: Having central air conditioning can add to the price 31,927.22 dollars.
* Land Contour_HLS: Having Significant slope from side to side can add 4,243.63 dollars to the price.
* Overall Cond: Higher the overall condition can add 1,737.31 dollars to the price.

**Top 3 Negative Coefficients**

* Land Contour_Lvl: Having Near Flat/Level can subtract -42,264.19 dollars to the price.
* Land Contour_Low: Having Low Depression can subtract -43,310.96 dollars to the price.
* Land Contour_Bnk: HAving Quick and significant rise from street grade to building can substract -72,620.47 to the price.

#### Explain the Random Forest Regressor

* **Using Festure Importance**

![png](/img/rf_feature_importance.png)

First of all, we can see that the most important feature is the GrLivArea, which is the above grade (ground) living area square feet. This is not surprising, as the bigger the house, the more expensive tend to be. Nonetheless we can see other features that have higher factor:

The 2 most important features are:
* Gr Liv Area: 0.44
* Total Bsmt SF:    0.36

The 4 following most important features are:
* Lot Area:         0.06
* Lot Frontage:     0.05
* Overall Cond:     0.03
* TotRms AbvGrd:    0.03

If we compare this features with the coefficients of the linear regression we can see different results here.

In linear regression the coefficient that push the price up is the Central Air_Y, but in the random forest regressor the most important feature is the GrLivArea, that have no important effect in linear regressionm model. The second most important feature is Total Bsmt SF, but in the linear regression the most important feature is Land Contour_HLS, which is not in the top 6 of the random forest regressor, and so on. This is because the random forest regressor is a non-linear model, and the linear regression is obviously a linear model. As it is not the purpose of this assignment to compare both models because, but the features analysis that we extract from the random forest regressor seems more reasonable about what you can see when you are buying a house.

By the way, the only feature that is in both most important features is Overall Cond.

* **Using SHAP.**

![png](/img/SHAP_feature_importance.png)

The top 6 most important features according to SHAP are:

* Gr Liv Area: this is the feature that have the most predictive power in the model. We can say that the greater the living area, the more expensive the house, and that's reasonable.

* Total Bsmt SF: We can say that the greater the basement area, the more expensive the house.

* Overall Cond: The red dots are concentrated around the 0 SHAP value, but we see a blue tail in the left side of the plot. This means that lower the overall conditions of the house have a negative impact in the price.

* Lot Area: We have a similar case that the Overall Cond,then we can conclude that the smaller the lot area, the lower the price.

* Lot Frontage: Red dots are in the right side of the plot, so the grater the lot frontage, the higher the price.

* Central Air_Y: Red dots are above the 0 SHAP Value, then we can say that having central air conditioning can add to the price.

### Part 2

* Plot a line graph of home values from states CA, WA, OR, AZ, NV, between years 2010 and 2020

![png](/img/mean_home_value_by_state_10-20.png)

We can see that the overall trend in Home Value is increasing, but we can see that the states of California and Washington are the ones that have the highest prices, and Arizona is the one that has the lowest prices.

### Part 3

Using Tableau make a:

* Bar graph of Median Home Value by Location.
* Line graph of % change in Home values by years.
* Highlight table of most expensive Zip Codes.
* Choropleth map of Median Home Value by Zip Code.

Tableau Visualizations can be found by clicking the link below:

[Visualizations: Home Prices](https://public.tableau.com/app/profile/israel.diaz/viz/shared/XPQ85743M)

---
 Thanks you
 