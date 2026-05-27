## Model Recommendations & Analysis

#### Best Model Selection

Among the tested models, XGBoost achieved the best performance on the validation dataset according to the F1-score metric. This model was therefore selected as the final model for prediction on the test dataset.

The superior performance of XGBoost can be explained by its ability to:

- Capture non-linear relationships between variables
- Handle interactions between features automatically
- Reduce overfitting through regularization
- Perform efficiently on structured tabular datasets

Compared to the baseline Logistic Regression model, XGBoost provided better balance between precision and recall, which is particularly important for optimizing the F1-score.



## Feature Importance Analysis

The analysis of feature importance shows that some variables have a much stronger impact on conversion prediction than others.

The most important feature appears to be:

- `total_pages_visited`

This suggests that user engagement is strongly correlated with conversion probability. Users visiting more pages are significantly more likely to subscribe to the newsletter.

Other moderately important features include:

- `country`
- `age`
- `source`

The variable `new_user` appears to have a smaller impact compared to browsing behavior variables.



## Model Strengths

The final model presents several advantages:

- Good predictive performance on unseen data
- Better handling of non-linear patterns
- Robustness against noisy features
- Ability to rank feature importance

The use of F1-score as the evaluation metric is appropriate because the dataset is imbalanced, meaning that converted users represent a minority of observations.



## Model Limitations

Despite good performance, the model still has some limitations:

- The dataset contains a limited number of features
- No temporal information is available
- The dataset may contain class imbalance
- The model could still overfit depending on hyperparameters
- User behavior is simplified to only a few variables

Additionally, feature importance does not necessarily imply causality.



## Possible Improvements

Several approaches could further improve model performance:

#### Hyperparameter Optimization

Using techniques such as:

- GridSearchCV
- RandomizedSearchCV

could improve model generalization and increase the F1-score.



#### Cross-Validation

Applying cross-validation would provide a more reliable estimate of model performance and reduce variance caused by a single train/test split.



#### Threshold Optimization

Since the competition metric is the F1-score, adjusting the prediction threshold instead of using the default threshold of 0.5 could improve the balance between precision and recall.



#### Additional Feature Engineering

Potential new features could include:

- Age groups
- Interaction variables
- Behavioral ratios
- Aggregated engagement metrics

Feature engineering may help the model capture more complex patterns.



#### Advanced Explainability

Using explainability tools such as SHAP values would allow deeper interpretation of the model predictions and improve transparency.



## Conclusion

This project demonstrates that machine learning models can effectively predict newsletter conversion behavior using a limited set of user features.

Among the evaluated models, XGBoost achieved the best overall performance and was selected as the final model. The analysis also highlighted the strong importance of user engagement variables, especially the number of visited pages.

Further improvements could still be achieved through hyperparameter tuning, feature engineering, and advanced explainability techniques.