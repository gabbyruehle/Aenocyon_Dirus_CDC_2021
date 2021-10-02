# Project Code Files

## 763K_AppData
This is the code for exploring the 763K_App dataset and creating graphs based on the number of apps released per month and the average price of apps released per month over the timerframe.

## Data_Cleaning_and_Logistic_model
This r script file contains the data cleaning operations to the original Worldwide Mobile App User Behavior survey including: removing unnecessary variables, removing incomplete curvey responses, and splitting the dataset into train and test datasets. This also has the cleaning of the maximum amount spent on an app variable (Q12_1 of original survey) which was used as the response variable for both models created. This variable was cleaned by removing unneeded symbols, translating different words to obtain country of origin, and converting the value by currency type so that the final variable was standardized to US dollars. This column was then used to create a binary column with 0 representing the person indicated spending no money on an app and 1 indicating the person surveyed has spent money on an app previously. 

The binary variables was tested against other variables in the dataset for association. The Mantel-Haenszel test was used for binary variables, the Chi-Square test for ordinal and nominal variables, and a logistic regression was used to check the 1 continuous variable. Only variables with a significant relationship to our binary target variable were used in model creation. 

The binary variable was used as the response variable to create different logisitic models from a variety of variable selction methods (backwards eliminaiton, stepwise selection). These models which were compared using different measures such as: concordance, ROC curves, KS statistic, and accuracy, and the final model was choosen based off these measures. The odds ratios from the final model were evaluated for recommendations and patterns for our presentation recommendations.

## Cumulative_Logit
This is the code for creating the Cumulative Logit Model from the Worldwide Mobile App User Behavior survey. The people surveyed who have spent money on an app were separted into 3 categories of 0< to 2, 2< to 5, and 5+ based on the amount of money they indicated. We created cumulative logit models to look at what characteristics were associated with higher monetary categories. These models were checked using the brant to ensure that a partial proportional odds model would not be a better fit. 

Different models were created based on variable selection techniques (backwards elimination with p-value and AIC, stepwise selection with AIC) and models were compared using an ANOVA test. Models were also compared using Notch charts which indicate the models' accuracy on the test dataset. The final model was choosen using these methods and was evaluated for recommendations and patterns for our presentation recommendations.
