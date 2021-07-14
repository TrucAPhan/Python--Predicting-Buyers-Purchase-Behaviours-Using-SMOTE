# Predicting Buyer's Purchase Behaviour Using SMOTE
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
     
<img width="273" alt="Screen Shot 2021-07-13 at 16 36 42" src="https://user-images.githubusercontent.com/63483928/125538548-cd26f283-e303-42b7-8ee8-ad9f814ba684.png">

   
   - Decision Tree: Since the relationship between between independent and outcomes of this dataset are complex, we then applied Decision Tree to forecast buyers' purchase behaviour. Decision trees appeared to perform better than traditional logistic when the relationship between independent and dependent variables are non-linear, which is the case in this dataset. However, decision tree are prone to overfitting, especially with small dataset, which is why we move on to Random Forest.
   
   <img width="332" alt="Screen Shot 2021-07-13 at 16 32 37" src="https://user-images.githubusercontent.com/63483928/125538209-c646e1ae-f0f1-43f3-a21f-c5136a0ef683.png">

   
   - Random Forest (**BEST MODEL**): Random Forest is one of the most versatile models which performs well under both classification and regression problem, or with categorical and continuous values. Although Random Forest is a continuation of decision trees, by introducing randomness to create a forest of trees, not only it can prevent the problem of overfitting of decision tree, but it also produces a more robust model. 

<img width="267" alt="Screen Shot 2021-07-13 at 16 39 14" src="https://user-images.githubusercontent.com/63483928/125538744-3d87a439-3662-401c-b2a8-9039a94fd386.png">

   - Our experiment with Gradient Boosting: Similar to Random Forest, but instead of building tree independently, Gradient Boosting builds one tree at a time. Also, while Random Forest combine results at the end by averaging/majority rules, Gradient Boosting combines results along the way. However, none of us had any experiences with Gradient Boosting, we did not not dive to deep into it.
  
3. Conclusion:
   - Random forest was the most appropriate and best model for this problem
     - Resilient to imbalanced data
     - Mix of categorical and continuous values
     - Builds upon Decision Tree, which provided decent initial results
   - SMOTE proved to be extremely useful
     - Helped improve recall power of the model greatly

