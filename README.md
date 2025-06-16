# **Biodegradable molecule classification models using open-source Galaxy**

## **Problem statement**

**Predicting Biodegradability Using Chemical Structures**

In this project, we will work on a classification problem related to biodegradation. Some chemicals break down very slowly, which can cause them to build up in the environment and become harmful. That’s why it's important to predict whether a chemical will break down quickly or not.
To do this, we use something called QSAR (Quantitative Structure-Activity Relationship) or QSPR (Quantitative Structure-Property Relationship). These are methods used to predict how a chemical behaves (like how fast it breaks down) based on its structure. 
In this project, we use molecular information (descriptors) to classify whether a molecule is **biodegradable** or **non-biodegradable** using supervised machine learning models.

## **Dataset source**
In this tutorial, we’ll use data from a study by [Mansouri et al](https://pubs.acs.org/doi/10.1021/ci4000213). in the journal of chemical information and modeling, based on information from a Japanese government agency. 
* Total compounds: 1055
* Classes: Biodegradable / Non-biodegradable
* Features: Precomputed molecular descriptors 

## **Method: Tools and Machine learning models**

We use **open-source Galaxy tools** to build classification models such as:
- Logistic Regression (LogReg)
- K-Nearest Neighbors (KNN)
- Random Forest (RF)

These models are evaluated based on their performance to help identify which algorithm works best for this classification task.


## **Results**

