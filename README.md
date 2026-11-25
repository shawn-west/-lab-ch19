# Tree-Based Models: Random Forests

## Objective

In this lab, I wanted to understand how random forests improve on single decision trees and linear regression when predicting house prices.

## Methodology

- Used the California Housing dataset to compare a single decision tree, OLS, Ridge regression, and random forests.
- Compared training and test RMSE and R² to identify overfitting.
- Examined how random forests combine multiple trees to improve predictions.
- Compared MDI and permutation importance to see which features mattered most.
- Used cross-validation to tune the forest's maximum depth and number of features considered at each split.
- Wrote my own AI prompt to create a reusable feature-importance chart and checked its results against my original calculations.

## Key Findings

- **Model performance:** The single tree had a test R² of 0.6228, Ridge had 0.5758, and the random forest performed best with 0.8046.
- **Overfitting:** The single tree had a training R² of 1.0 but a much lower test R², showing that it was overfitting the training data.
- **Feature importance:** Latitude scored 0.0890 with MDI but 0.4427 with permutation importance. This showed me that the two methods can rank features differently.
- **Model tuning:** Cross-validation selected an unlimited tree depth and `max_features=0.5`. The tuned forest reached a test R² of 0.8094.
- **AI-assisted coding:** I used two rounds of prompting to create a feature-importance function. Both rounds passed every check, matching the original importance values with 0% difference, including tests on another decision tree.

## Conclusion

This lab showed me why random forests can perform better than single trees and linear regression. While a single tree can memorize training data, a forest combines multiple trees to make better predictions on new data.

I also learned that feature importance depends on how it's measured and that cross-validation can help improve model performance without relying only on training accuracy.
