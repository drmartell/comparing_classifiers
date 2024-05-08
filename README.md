# Comparing Classifiers

This repository explores the usage of various classification methods, specifically
- k-nearest neighbors
- logistic regression
- decision trees
- support vector machines

in a binary classification problem:
Whether or not a Portuguese banking customer will be upsold into a term deposit product.

The UCI dataset can be found here:
https://archive.ics.uci.edu/dataset/222/bank+marketing

More details can be found in the [Jupyter notebook](comparing_classifiers.ipynb), here is a summary of some key metrics:



| Model               | AUC    | Precision | Recall | F1-Score |
| ------------------- | ------ | --------- | ------ | -------- |
| Logistic Regression | 0.9005 | 0.63      | 0.33   | 0.43     |
| SVM                 | 0.8844 | 0.67      | 0.33   | 0.44     |
| KNN                 | 0.8251 | 0.60      | 0.34   | 0.44     |
| Decision Tree       | 0.6907 | 0.45      | 0.45   | 0.45     |


<br>The top contending models were SVM and Logistic Regression.


Although the SVM model had the highest precision and strong AUC. On balance, Logistic Regression is recommended in this case due to its even higher AUC and explainability.

The feature coefficients of the Logistic Regression model would indicate a few strategic considerations for the marketing team.

1. The time of year that campaigns are run appears influencial with March being the month that most increases the odds of success and January being the least.
2. Prior success or failure of campaigns with a given customer is also a strong indicator of current success.
3. Longer duration conversations have been more successful.

<br>Next steps might include:
- concentrating marketing campaign in the most successful months
- testing differing messaging for those customers who've purchased in the past vs. those who have not
- exploring some of the techniques that sales reps with longer conversation durations are utilizing and building training around the findings

