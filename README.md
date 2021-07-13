# Predicting Purchase Buyer's Behaviour Using SMOTE
This is my academic group project. Due to privacy concerns, data and some part of the code will not be published.

## Problem description:
Predicting whether certain buyers will buy a product (YES) or not (NO) (Classification Problem)

## What is SMOTE?
**Synthetic Minority Oversampling Technique**, also known as **SMOTE**, is a type of data augmentation used to oversample the minority class in an imbalanced dataset. The problem with an imbalanced dataset is that there is very few data of the minority class (in this case, the buyers that were predicted to buy (YES) only accounted for less than 0.5% of the dataset) for the models to be effectively trained.

## Machine Learning Procedures:
1. EDA:
   - Process missing values
   - Variables selection according to the Confusion Matrix
   - Convert negative values to zeros
   - Process outliers: drop rows with stardard deviation greater than 2
2. Modeling & Results:
   - Logistic Regression: First, we applied logistic regression since it is well-known for modeling binary classification problem. Since it’s relatively simple, we used this model as a baseline model for more complex ones.
        <img width="281" alt="Screen Shot 2021-07-13 at 16 30 25" src="https://user-images.githubusercontent.com/63483928/125538038-3ce1af9a-d84f-4b62-b2b1-f63f01176032.png">
   
   - Decision Tree: Since the relationship between between independent and outcomes of this dataset are complex, we then applied Decision Tree to forecast y_buy. Decision trees appeared to perform better than traditional logistic when the relationship between independent and dependent variables are non-linear, which is the case in this dataset. However, decision tree are prone to overfitting, especially with small dataset, which is why we move on to Random Forest.
   - Random Forest (**BEST MODEL**): Random Forest is one of the most versatile models which performs well under both classification and regression problem, or with categorical and continuous values. Although Random Forest is a continuation of decision trees, by introducing randomness to create a forest of trees, not only it can prevent the problem of overfitting of decision tree, but it also produces a more robust model. 
   - Our experiment with Gradient Boosting: Similar to Random Forest, but instead of building tree independently, Gradient Boosting builds one tree at a time. Also, while Random Forest combine results at the end by averaging/majority rules, Gradient Boosting combines results along the way. However, none of us had any experiences with Gradient Boosting, we did not not dive to deep into it 
3. Results
4. Recommendation
