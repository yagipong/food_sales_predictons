# Food Sales Predictions

Sales are partially predictable, but with some caveats

Author: Yaw Agipong

Business problem:

How can we predict food sales given a series of features related to item sales?

Data:

The source data was the sales_prediction.csv 

https://drive.google.com/file/d/1syH81TVrbBsdymLT_jl2JIf6IjPXtSQw/view

Methods

The project used several methods to process the data and draw out trends, including but not limited to:
- data cleaning
- exploratory and explanatory visualizations (boxplots, heatmaps, bar graphs)
- machine learning preprocessing

Results

![Unknown-2](https://user-images.githubusercontent.com/105327648/202651232-40abc3be-44b1-45f5-a8fb-f6672418c329.png)

Correlation Heatmap

The Correlation Heatmap demonstrates that most of the variables are not highly correlated, except for Item Outlet Sales and Item MRP.

![Unknown-3](https://user-images.githubusercontent.com/105327648/202651676-bc982c2b-39de-411d-a2fb-05667bef65e8.png)

Bar Graph - Item Fat Content vs. Item Visibility

The bar graph displays the relatively similar visibility between low fat and regular items.

Model

The final model was a regression between the most relevant features and the item sales. The most important metric from this regression was the R^2 value for both the training data and the testing data. Both the training data and testing data featured an R^2 value around .56, indicating that the model was well balanced but only accounted for some of the variation betwen the variables. Therefore, the identified features are only moderately useful predicting sales.

![random_forest_importances](https://user-images.githubusercontent.com/105327648/221492422-5182b6c7-ea59-4b04-9684-4341ba170125.png)

The importances derived from a Random Forest Regression demonstrate that Item_MRP was by far the most important feature in the model.


![lin_reg_coeffs](https://user-images.githubusercontent.com/105327648/221492609-0c6efe92-53bd-4c3f-90b7-20f9d56c9928.png)

As these coefficients are not scaled, the coefficient with the largest positive impact on food sales was the outlet establishment year. The other most impactful features negatively impacted food sales.

![bar](https://user-images.githubusercontent.com/105327648/221834184-d5a31912-03d4-4317-8706-5eb26a9689f4.png)

![dot](https://user-images.githubusercontent.com/105327648/221834225-ee87a065-4cee-44bc-9f26-78eaff70631a.png)

The Shap plots reinforce the conclusion from the importances graph, namely that Item_MRP is the most important predictive feature for this model.

Recommendations:

The most important recommendation is to find variables that can better predict sales. The current slate of variables only provides moderate predictive capability, which is not very useful in a business setting.

For further information

For any additional questions, please contact yagipong@outlook.com
