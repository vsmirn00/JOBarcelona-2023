### Readme for Jobarcelona 2023 Competition

### Introduction:
The Jobarcelona 2023 Competition was organized by Nuwe. The competition required participants to use diverse methodologies to analyze the given dataset and to build a model to predict the attrition flag. In this competition, a stacking algorithm was used, which overlapped a logistic regression on a SVM and Random Forest model to improve the accuracy of the predictions. First off, the idea was to use a gradient boosting algorithm. But, for the sake of experimentation, I decided to use stacking.

### Methodologies used:
Participants in the competition used a range of methodologies to analyze the given dataset in the part of exploratory data analysis. In my case, I included univariate analysis and bivariate analysis with scatterplots and correlation matrices. I experimented with dimensionality reduction and clustering algorithms such as PCA with K-means and GMM to encode new variables to increase the models' precision. However, this did not yield much success. 

### Feature selection:
Feature selection was performed based on features with correlation above 0.1 or below -0.1 with the target variable. Multicollinearity was measured only to select uncorrelated features. In the end, the clusters were not significant for the prediction. Furthermore, anomaly detection was performed thanks to this clustering process. I detected a wide proportion of outliers above the 95 percentile and below the 5 percentile. Therefore, I tried to encode it into a new cluster and also to remove it from the training dataset. This was performed with the aim of improving the models capability to generalize. However, it did not bring sufficiet improvement, so the final model simply was build without the cluster label and with all the outliers included as part of the original distribution of data. Regarding multicollinearity, this measure was used to identify the most relevant features for the model and to eliminate any redundant features that might have been included.

### Results:
The results of the competition were saved in the file "predictions.json." The model built using the stacking algorithm had the highest accuracy in predicting the attrition flag. To evaluate the resuslts, ROC-AUC was plotted to evaluate the 3 base algorithms separatedly against the stacking of the three. SVM and the stacked algorithms yielded the best results, accounting for an accuracy of 0.82 both of them. 

### Conclusion:
The Jobarcelona 2023 Competition was a great opportunity for participants to test their skills in data analysis and modeling. The use of diverse methodologies and feature selection techniques helped me to improve the accuracy of my predictions and my skillset as a Data Scientist. Overall, the competition was a great success, and I look forward to more competitions in the future.
