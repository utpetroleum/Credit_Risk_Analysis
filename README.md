# Credit_Risk_Analysis

## Overview of Project

### Purpose

Using the credit card credit dataset from LendingClub, we oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. In the end, we evaluate the performance of these models and make a recommendation on whether they should be used to predict credit risk.

## Results

1. RandomOverSampler
	* The balanced accuracy score was 0.6573
	* The high risk precision and recall scores were 0.01 and 0.71
	* The low risk precision and recall scores were 1.00 and 0.60

![ROS_bas](https://user-images.githubusercontent.com/92401000/154891389-3b2b80ea-3828-4d5c-8f7c-cdc009253cae.PNG)

![ROS_cri](https://user-images.githubusercontent.com/92401000/154891394-43b1b6fa-4c77-4423-939d-c74b28451da7.PNG)

2. SMOTE
	* The balanced accuracy score was 0.6622
	* The high risk precision and recall scores were 0.01 and 0.63
	* The low risk precision and recall scores were 1.00 and 0.69

![SMOTE_bas](https://user-images.githubusercontent.com/92401000/154891506-5baf3068-9b7e-4be6-a26d-342ce40c064f.PNG)

![SMOTE_cri](https://user-images.githubusercontent.com/92401000/154891518-01453634-4d69-46de-b0f2-15f8ad347406.PNG)

3. ClusterCentroids
	* The balanced accuracy score was 0.5443
	* The high risk precision and recall scores were 0.01 and 0.69
	* The low risk precision and recall scores were 1.00 and 0.40

![CC_bas](https://user-images.githubusercontent.com/92401000/154891562-834d2086-ab97-48b9-ba7d-6a09ebe489b5.PNG)

![CC_cri](https://user-images.githubusercontent.com/92401000/154891571-375c9851-2ed9-4be4-8d37-7db25747ec24.PNG)

4. SMOTEENN
	* The balanced accuracy score was 0.6392
	* The high risk precision and recall scores were 0.01 and 0.70
	* The low risk precision and recall scores were 1.00 and 0.58

![SMOTEENN_bas](https://user-images.githubusercontent.com/92401000/154891615-f7b3a0a0-00cd-436a-9771-5382a80b024c.PNG)

![SMOTEENN_cri](https://user-images.githubusercontent.com/92401000/154891626-9092c532-e32c-4129-a6fd-d8e31e4fe9af.PNG)

5. BalancedRandomForestClassifier
	* The balanced accuracy score was 0.7885
	* The high risk precision and recall scores were 0.03 and 0.70
	* The low risk precision and recall scores were 1.00 and 0.87

![BRFC_bas](https://user-images.githubusercontent.com/92401000/154891675-8b44450f-779b-4136-993b-a1d6dbdc6121.PNG)

![BRFC_cri](https://user-images.githubusercontent.com/92401000/154891682-5ebcf803-d772-4b70-80bf-fda1fc4ab0ca.PNG)

6. EasyEnsembleClassifier
	* The balanced accuracy score was 0.9317
	* The high risk precision and recall scores were 0.09 and 0.92
	* The low risk precision and recall scores were 1.00 and 0.94

![EEC_bas](https://user-images.githubusercontent.com/92401000/154891723-f8ff4b09-4405-4537-93c1-e15e68836a3e.PNG)

![EEC_cri](https://user-images.githubusercontent.com/92401000/154891734-61a4986a-230b-4638-9ed7-9a2cc6bbc8d7.PNG)

## Summary

In terms of balanced accuracy scores, oversampling resamplers did slightly better than undersampling resampler (ClusterCentroids) by 0.1. The combination sampling SMOTEENN performed the same as oversampling in the 0.6 range. The two ensemble algorithms performed the best in terms of balanced accuracy scores, with EasyEnsembleClassifier performing the best at 0.9317.

The precision for high risk and low risk for the oversampling resamplers, undersampling resampler, and combination sampling SMOTEENN were the same at 0.01 and 1.0. The precision for high risk for the two ensemble algorithms BalancedRandomForestClassifier and EasyEnsembleClassifier increased slightly at 0.03 and 0.09. 

The recall for high risk and low risk for the oversampling resamplers, undersampling resampler, and combination sampling SMOTEENN fluctuate between 0.6 and 0.7 with ClusterCentroids having the lowest low risk recall at 0.40. The recall for high risk and low risk for the two ensemble algorithms BalancedRandomForestClassifier and EasyEnsembleClassifier performed better with EasyEnsembleClassifier having a high risk and low risk recall of 0.92 and 0.94.

The model I recommend is EasyEnsembleClassifier. It has the highest balanced accuracy score of 0.9317 and highest high risk precision and recall scores of 0.09 and 0.92 and low risk precision and recall scores of 1.00 and 0.94 