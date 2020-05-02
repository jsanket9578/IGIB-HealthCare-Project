# IGIB-HealthCare-Project

Project Aim: To predict "Gestational Age" of 3 women based on the 7 multi-omics high-dimensional datasets. Training data consist of 14 women.
More details can be found here: https://github.com/rintukutum/challengeLab-ML
      
<img src= "https://raw.githubusercontent.com/rintukutum/challengeLab-ML/master/figures/figure-01.png">

# Observations and Results:
1. Number of features are much more than the number of samples so simple models like LinearRegression and RandomForests attempted.
2. For some records, Gestational Age is negative (Measurement taken after pregnancy) which is difficult for the model to predict.
3. Some datasets had more than 50000 features. Feature selection was performed for such cases, removing features on the basis of variance and correlation, and selecting the top 100 features. The results didn't degrade by much, signifying that majority of the features are irrelevant and exhibit low correlation with the target.
4. Mean Absolute Error comes out to be 3.2, 2.9, 1.4 years for the 3 sub-challenges respectively. This reveals that individually datasets in parts 1 and 2 don't perform that well and it is the combination of both of these that leads to good results.

# Key Takeaways:
1. When features available are much more than data points, it doesn't make sense to use a Neural Network based model but instead try eleminating features using liner/non-linear methods.
2. Building weak models in an ensemble for regression may not be ideal, since the only option for computing the output is average of all of them.

