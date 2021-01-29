# Credit_Risk_Analysis

## Overview of Analysis

- For this project, we wanted to analyze the different factors that are taken into consideration when determining Credit Risk. This would give us insight as to what plays into determining which candidates would be considered high risk or low risk. 

- In our analysis we used several different models and sampled the data in different ways.

- First we decided to utilize scikit-learn and imbalanced-learn to build and evaluate models using resampling as follows below
- The next part included oversampling using RandomOverSampler and SMOTE algorithms
- We then undersampled the data using ClusterCentroids resampler algorithm
- After that, we wanted to use a combination of both over- and undersampling. For this we used SMOTEENN algorithm
- Once we completed this, our final task was to compare two different machine learning models to reduce bias in our data. For this we used BalancedRandomForestClassifier and EasyEnsembleClassifier. 

## Results

### Naive Random Oversampling

<img width="860" alt="Screen Shot 2021-01-29 at 10 38 23 AM" src="https://user-images.githubusercontent.com/68168883/106295316-4587ca00-621e-11eb-8e88-5513bd72e594.png">

- Our balanced accuracy score was 64%, which is not particularly strong
- The overall precision was 99%, however was extremely low for high risk candidates at only 1%. 
- The recall for high risk was 66% and 62% for low risk. This indicates that our true positive predictions are also relatively low. 
- The F1 score was 76%, which is a measure that reconciles the precision and recall.

### SMOTE Oversampling

<img width="855" alt="Screen Shot 2021-01-29 at 10 47 27 AM" src="https://user-images.githubusercontent.com/68168883/106296256-6dc3f880-621f-11eb-9cd0-207db4f04db3.png">

- Using this oversamping method, our balanced accuracy score was 65.1%, which is slightly but not significantly better than our previous model. 
- We found the same overall precision marks at 99% overall. 
- The recall for high risk was 61%, which was lower but for low risk went up to 69%. 
- Here however, our F1 went up to 81%. 

### Undersampling

<img width="862" alt="Screen Shot 2021-01-29 at 10 54 02 AM" src="https://user-images.githubusercontent.com/68168883/106297040-55081280-6220-11eb-967f-5a453a5d2908.png">

- Here we undersampled the data and found our balanced accuracy score to be 64.5%.
- The overall precision remained the same.
- Recall for high risk stayed in the general vicinity of our previous models at 67% but the low risk noticeably went down to 42%.
- Likewise, since our recall overall decreased precipitously, so did our F1 value, down to 58%. 

### Combination (Over and Under) Sampling

<img width="862" alt="Screen Shot 2021-01-29 at 10 54 02 AM" src="https://user-images.githubusercontent.com/68168883/106297467-bc25c700-6220-11eb-9e5c-d6274cba360a.png">

- In this test, we used SMOTEENN to resample our data and found that the balanced accuracy was 54.4%, the lowest thus far.
- Overall precision also remained the same at 99% overall and 1% for high risk and 100% for low risk.
- The recall for high risk went to our highest level thus far at 72% and low risk was on the low end at 57%. 
- As we would expect based on recall, the value for our F1 was much better than undersampling but still lower than we saw previously at 72%. 

### Balanced Random Forest Classifier 

<img width="851" alt="Screen Shot 2021-01-29 at 11 02 38 AM" src="https://user-images.githubusercontent.com/68168883/106298359-cc8a7180-6221-11eb-9e79-6b059c284ce3.png">

- Here we used the Balanced Random Forest Classifier and our balanced accuracy score was 76.4%.
- Our overall precision was but we noticed that the high risk went up slightly to 3%. 
- The recall for high was was only 63% but the low risk was much higher at 89%.
- Because our recall went up, our F1 reached a new high at 94%. 

### Easy Ensemble AdaBoost Classifier

<img width="844" alt="Screen Shot 2021-01-29 at 11 02 50 AM" src="https://user-images.githubusercontent.com/68168883/106298367-cf856200-6221-11eb-9b8f-a9939945cf38.png">

- In our final model, using Easy Ensemble, our balanced accuracy shot up to 91.5%
- Our overall precision was 99% and saw that high risk precision went up even a little more to 5%. 
- The recall for high risk shot up to 93% and low risk to 90%, representing highs for both measures.
- Our F1 remained at 94%, but still much better than the non-ensemble methods of resampling the data.

## Summary

In trying to determine which loans would be considered high or low risk, we resampled our data using 6 different models. We used 4 models of resampling, which included oversampling, undersampling and a combination of both and these models provided modest results. When we switched to ensemble classifiers, our results were significantly better. While Balanced Random Forest did produce very good results, Easy Ensemble demonstrated a better representation of recall and precision so our recommendation for a machine learning model would be to use the Easy Ensemble Classifier. 
