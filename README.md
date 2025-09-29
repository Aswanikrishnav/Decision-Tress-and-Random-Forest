# Decision Tree and Random Forest-Heart Disease
## Overview


This project demonstrates the use of tree-based machine learning models for classification tasks, specifically predicting the presence of heart disease. It uses Decision Trees and Random Forests on the Heart Disease dataset to illustrate model training, evaluation, feature importance, and overfitting analysis.

## Dataset
The dataset contains clinical attributes of patients such as age, sex, chest pain type, resting blood pressure, cholesterol, maximum heart rate, and more.

Target Variable:

0 → No heart disease

1 → Heart disease present

## Objective


1. Train a Decision Tree Classifier to predict heart disease.

2. Visualize the tree and interpret splits.

3. Analyze overfitting by evaluating model performance at different tree depths.

4. Train a Random Forest Classifier and compare its performance with the Decision Tree.

5. Identify and interpret feature importances from the Random Forest.

6. Evaluate model performance using cross-validation.


## Tools and Libraries

python,
numpy, 
pandas, 
matplotlib, 
scikit-learn

## Project Workflow

The project begins with data acquisition and preprocessing. The Heart Disease dataset was loaded from a CSV file, and the features (X) and target variable (y) were separated. The data was inspected for missing values and categorical variables, ensuring it was ready for model training. The dataset was then split into training and testing sets to allow proper evaluation of model performance.

Next, a Decision Tree Classifier was trained on the training set. The tree structure was visualized to understand how the model splits the data based on feature thresholds. To analyze potential overfitting, the Decision Tree was trained with varying max_depth values, and both training and testing accuracy were plotted. This analysis helped identify the optimal tree depth that balances bias and variance, preventing underfitting and overfitting.

Following this, a Random Forest Classifier was implemented. Random Forests create an ensemble of multiple decision trees, which improves generalization and reduces the risk of overfitting compared to a single decision tree. The Random Forest model was trained on the same dataset, and its accuracy was evaluated and compared with the Decision Tree.

An important step was interpreting feature importances from the Random Forest model. By analyzing the importance scores, the project identified which clinical features—such as chest pain type, maximum heart rate, and ST depression—had the strongest influence on predicting heart disease. Finally, cross-validation was performed to assess model performance more reliably across multiple folds of the data. This ensured that the observed accuracy was not dependent on a specific train-test split.


## Results


The Decision Tree Classifier achieved a test accuracy of approximately [0.98], demonstrating good predictive ability but showing signs of overfitting when the tree depth was increased too much. The Random Forest Classifier outperformed the single tree, achieving a higher accuracy of approximately [0.98]. This improvement highlights the advantage of aggregating multiple trees to reduce variance and improve generalization.

The feature importance analysis revealed that features such as chest pain type (cp), maximum heart rate achieved (thalach), and ST depression (oldpeak) were the most influential predictors of heart disease. Less important features contributed minimally to the model’s decisions, which aligns with clinical knowledge about cardiovascular risk factors.

Cross-validation confirmed the robustness of these models. The Random Forest maintained high performance across folds, indicating stable generalization, whereas the Decision Tree showed more variability, particularly when the tree was deep. Overall, the project demonstrated that tree-based models can effectively classify heart disease, while Random Forests provide better accuracy and resilience against overfitting.

## Conclusion

- Decision Trees are simple and interpretable but prone to overfitting.
  

- Random Forests reduce overfitting by combining multiple trees.
  

- Feature importance analysis helps identify key clinical indicators of heart disease.
  

- Cross-validation provides a robust estimate of model performance.
