# Recovered_gold_share_prediction_model
## Integrated project 2 from Practicum by Yandex

### Goal

Develop a machine learning model for Zyfra, efficiency solutions for heavy industry company, that would analyze data on extraction and purification of gold from an ore and predict the amount of recovered gold. The model will help to optimize the production and eliminate unprofitable parameters.

### This project's repo includes the following files:

- The project's jupyter notebook (Recovered_gold_share_prediction_model.ipynb);
- A pdf format of the notebook (Recovered_gold_share_prediction_model.pdf);
- Input data (gold_recovery_train.csv, gold_recovery_test.csv, gold_recovery_full.csv);
- Project description from Practicum (IP2_project_description.pdf);
- Metrics pictures (Final_sMAPE.png, gold_recovery_process.png, recovery_calculation.png, sMAPE.png).

### This project includes the following steps:

1. Descriptive statistics;
2. Recovery calculation check;
3. Missing features analysis;
4. Data Preprocessing;
5. EDA: outliers and target variable analysis;
6. Features standard scaling;
7. Models' hyperparameters tuning;
8. Model selection;
9. Feature importances;
10. Sanity check.

### Based on the analysis (EDA) we have come to the following conclusions:

- As for the gold concentration (au), there is a clear trend towards quality improvement after each stage: the share of gold is higher and higher on average as we proceed with purification (from 20% to more than 45%, on average);
- Interestingly, we see the opposite trend for silver concentration (ag): the more we purify the feed, the lower gets the share of this metal (from around 11% to less than 5%, on average);
- As for the lead concentration (pb), we can say that there is probably no need for the second purification stage, as the quality of this metal doesn't improve, on average. However, we see a slight improvement after the first stage (from around 8% to almost 11%, on average);
- The train and test distributions of feed particle sizes are very close to each other, which means that we will not have a problem of applying a model trained on the train set to the test set;
- We found some outliers in the target variables and removed them.

In the next step we developed and tested, using cross-validation, several **ML algorithms and tuned the best model's hyperparameters**. Lasso regression model showed the lowest score. 

The selected model appeared to be overfitting to the train set, so we decided to implement **feature selection** method to reduce the overfitting. We have measured feature importances using the coefficients from the Linear Regression model and identified the most profitable parameters.

Then we have tested our model on the test set. We have reached **6.8% error rate on the test set**.

Finally, we have checked our model for **sanity** by comparing the final score to the baseline score. The final score of our model is lower (by 11%) than the baseline score.

### The logbook of this project can be found [here](https://docs.google.com/spreadsheets/d/1SrGdReexaSEomJGS6yR6cRwJtHA_XqpprnLaE7B6Ayg/edit#gid=1260390115) (IP2 tab).
Total time spent on the project: 13.6 hours with a daily average of 2.73 hours working for 5 days.
