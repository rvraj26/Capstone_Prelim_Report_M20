## Semiconductor Wafer Fab Yield Classification - Prelim Report

**Raj Varada**

#### Research Question
What are you trying to answer?

The project addresses the following research question: Given the sensor data from a semiconductor wafer fab, how can a wafer be classified as yielding or not, and how can this be predicted early to save cost and time? 


#### Data Sources
What data will you use to answer your question?

The data for this research is sourced from the UCI data repository and is at https://archive.ics.uci.edu/dataset/179/secom
This is the only public data source I could find. There are less than a handful of state-of-the-art semiconductor wafer fabs, and the data is very tightly controlled.

#### Methodology
What methods are you using to answer the question?

CRISP-DM is the structured framework used for problem-solving. The project also uses the following methodologies and algorithms. 

	1. Exploratory Data Analysis: Various methods to visualize data to identify data preparation requirements
	2. Data Preparation: Various data cleaning methods like imputing, scaling, outlier elimination, dropping some data, addressing collinearity in the data
	3. Classification: The following classifiers are used:
		a. Dummy Classifier (DC): This will be the baseline model. 
		b. Decision Tree Classifier (DTC): 
		c. Logistic Regression (LR)
		d. Simple Vector Model (SVM)
		e. Random Forest Classifier (RFC)
		f. K-Nearest Neighbor Classifier (KNN)
		g. Naïve Bayes Classifier (NB)
	4. Cross-validation using Stratified KFold. This method is used because the dataset is quite imbalanced. 
	5. Hyperparameter Tuning using parameter grid search

Extensive data reporting and plotting are implemented to validate the code and visualize the results. 

#### Results
What did your research find?

Final Result

Support Vector Machines (SVM) classifier performed the best for this wafer fab yield problem. Random Forest produced similar results but had a significantly higher run time. The recommendation is to use SVM with the best parameter reported above.

Method	Accuracy	Precision	Recall	F1-score
Support Vector Machines	0.9337	0.93	1.00	0.96
KNearest Neighbors	0.9260	0.94	0.99	0.97
Random Forest	0.9337	0.93	1.00	0.97

The confusion matrix for the SVM result is below. 

#### Outline of project

- [Link to notebook 1]()


