# **Biodegradable molecule classification models using open-source Galaxy**

## **Problem statement**

**Predicting Biodegradability Using Chemical Structures**

In this project, we will work on a classification problem related to biodegradation. Some chemicals break down very slowly, which can cause them to build up in the environment and become harmful. That’s why it's important to predict whether a chemical will break down quickly or not.
To do this, we use something called QSAR (Quantitative Structure-Activity Relationship) or QSPR (Quantitative Structure-Property Relationship). These are methods used to predict how a chemical behaves (like how fast it breaks down) based on its structure. 
In this project, we use molecular information (descriptors) to classify whether a molecule is **biodegradable** or **non-biodegradable** using supervised machine learning models.

## **Dataset source**
In this tutorial, we’ll use data from a study by [Mansouri et al](https://pubs.acs.org/doi/10.1021/ci4000213) in the Journal of Chemical Information and Modeling. 
* Total compounds: 1055
* Classes: Biodegradable / Non-biodegradable
* Features: Precomputed molecular descriptors 

## **Method: Tools and Machine learning models**

We use **open-source Galaxy tools** to build classification models such as:
* Logistic Regression 
* K-Nearest Neighbors (KNN)
* Random Forest (Bagging) 

These models are evaluated based on their performance to help identify which algorithm works best for this classification task.


## **Results**

**Logistic Regression Performance**

![logreg_confusion matrix](https://github.com/harishmuh/Biodegradarable-molecules_classification_Galaxy/blob/main/documentation/logreg_confusion_matrix.png?raw=true)

![logreg Precision, recall, f-score curve](https://github.com/harishmuh/Biodegradarable-molecules_classification_Galaxy/blob/main/documentation/logreg_precision_recall_linear.png?raw=true)

![logreg roc auc](https://github.com/harishmuh/Biodegradarable-molecules_classification_Galaxy/blob/main/documentation/logreg_roc_linear.png?raw=true)

**KNN Performance**

![knn confusion matrix](https://github.com/harishmuh/Biodegradarable-molecules_classification_Galaxy/blob/main/documentation/knn_confusion_matrix_NN.png?raw=true)

![knn Precision, recall, f-score curve](https://github.com/harishmuh/Biodegradarable-molecules_classification_Galaxy/blob/main/documentation/knn_precision_recall_NN.png?raw=true)

![knn roc auc](https://github.com/harishmuh/Biodegradarable-molecules_classification_Galaxy/blob/main/documentation/knn_roc_NN.png?raw=true)

**Random Forest (Bagging) Performance**

![rf_confusion matrix](https://github.com/harishmuh/Biodegradarable-molecules_classification_Galaxy/blob/main/documentation/rf_confusion_matrix_bagging.png?raw=true)

![rf Precision, recall, f-score curve](https://github.com/harishmuh/Biodegradarable-molecules_classification_Galaxy/blob/main/documentation/rf_precision_recall_bagging.png?raw=true)

![rf roc auc](https://github.com/harishmuh/Biodegradarable-molecules_classification_Galaxy/blob/main/documentation/rf_roc_bagging.png?raw=true)

**Summary table**

| Model            | ROC-AUC |
|------------------|---------|
| Logistic Reg.    | 0.94    |
| K-Nearest Neigh. | 0.95    |
| Random Forest    | 1.00    |

**Insights**

* The model evaluation based on ROC-AUC (Receiver Operating Characteristic - Area Under Curve) shows how well each classifier distinguishes between biodegradable and non-biodegradable molecules.
* All three models performed very well, with ROC-AUC scores above 0.90, indicating high classification performance.
* The Random Forest model achieved a perfect ROC-AUC score of 1.00, suggesting it was able to completely distinguish between the two classes without error on the test set.
* KNN slightly outperformed Logistic Regression, but the difference is minor (0.95 vs. 0.94), showing both models can serve as good alternatives when simpler or interpretable models are preferred.
* These high scores across models may indicate that the molecular descriptors used provide strong predictive features for biodegradability.

## **Conclusion**
The results suggest that these machine learning models, particularly Random Forest, are highly effective in predicting biodegradability from molecular descriptors. While Random Forest offers the best performance, Logistic Regression and KNN still show strong predictive capability and might be preferred in cases where interpretability or lower computational cost is important.


