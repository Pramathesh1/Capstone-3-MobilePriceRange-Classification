# Mobile Price Range Classification
## Business Problem
In the competitive mobile phone market companies want to understand sales data of mobile phones and factors which drive the prices. The objective is to find out some relation between features of a mobile phone(eg:- RAM, Internal Memory, etc) and its selling price. In this problem, we do not have to predict the actual price but a price range indicating how high the price is.

## Summary
This classification project aimed to predict the price range of mobile phones based on features such as battery power, RAM, internal memory, and screen size. The project was carried out in several steps, including preliminary data exploration and data wrangling, exploratory data analysis and data visualization, hypothesis testing, feature engineering, model implementation, and use of explainability tool.

### EDA
The dataset was explored to identify any missing or erroneous data points, and data wrangling techniques were employed to clean the dataset. Exploratory data analysis was then conducted to identify any patterns or trends in the data. The analysis revealed that RAM was the main feature to affect the mobile phone price range.

### Hypothesis Testing
Hypothesis testing was performed to validate the observations of the EDA phase. Hypothesis testing was conducted to determine whether there was a significant impact on the output by the features of RAM, battery power and 4G connectivity. The results showed that RAM and battery power did have a significant impact on the output, but output was not affected significantly by 4G connectivity.

### Data Preprocessing
In the next step, feature engineering was performed to modify existing features that would improve the predictive performance of the model. Then, the features were separated into dependent and independent variables to make it easier for model implementation. Also the data was scaled for linear regression.

### ML Model Implementation
Four different classification models were trained and evaluated on the dataset, namely Decision Tree, Random Forest, XGBoost and K-Nearest Neighbor (KNN). The evaluation metrics used were accuracy, precision, recall, F1-score, and the Area Under the Receiver Operating Characteristic Curve (AUC-ROC). The results showed that KNN outperformed the other models, achieving the highest accuracy, precision, recall, F1-score, and AUC-ROC. The hyperparameters of each model were also tuned using grid search to identify the optimal hyperparameters.

The hyperparameters of each model were also tuned using grid search to identify the optimal hyperparameters. The KNN model was also tuned using grid search. The results showed that the KNN model achieved an accuracy of 92.53% and roc-auc score 99.05% before tuning and accuracy 92.96% and roc_auc score 99.16% meaning there is very less, almost negligible improvement in performance of model. Added to that, the tuned KNN model overfits with 100% accuracy on train set. So using tuned KNN model is not recommended.

### ShAP Explainers
To gain insights into the factors that influenced mobile phone price range, feature importance analysis was conducted using the SHapley Additive exPlanations (SHAP) method. The analysis revealed that RAM was the most important feature in predicting mobile phone price range, followed by battery power, pixel width and pixel height. The force plots also explained how the probability of getting each class as output is affected by which feature and what impact the features have on the output.

## Conclusion
1.	K-nearest Neighbors algorithm has performed the best classification on this data, followed by XGboost with test accuracy of 92.53% and roc-auc score of 0.9905. 
2.	RAM is the most important feature which decides the classification. Battery power, Pixel-width and pixel height are the next most important features. RAM and pixel height try to keep the output to 'High Cost' while battery power and pixel width push the output to as high as they can. 
3.	Every algorithm has performed best classification for the extreme classes of 'Low Cost' and 'Very High Cost' and performed relatively bad for the middle classes of 'Medium Cost' and 'High Cost'.

In conclusion, this project demonstrates the effectiveness of machine learning techniques in analyzing and predicting complex systems such as mobile phone pricing. The KNN model outperformed other models, and RAM was identified as the most important feature for accurate predictions. The findings of this project can be used by mobile phone manufacturers to optimize their pricing strategies and to develop mobile phones with the desired features to meet customer demands. Overall, this project highlights the importance of data preprocessing, feature engineering, and explainability tools in developing accurate and interpretable machine learning models.
