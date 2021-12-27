# Credit_Risk_Analysis

### Overview

The purpose of this project was to use multiple machine learning algorithms to predict credit risk. The algorithms are RandomOverSampler and SMOTE, ClusterCentroids, the combined approach of SMOTEENN, and BalancedRandomForestClassifier and EasyEnsembleClassifier. 

### Results

### Definitions 
Precision - A measurement that specifies what fraction of the machine-learning annotator's output was accurate when compared to the human annotator output. Precision is determined by the number of correctly labeled annotations divided by the total number of annotations added by the machine-learning annotator. A precision score of 1.0 for entity type A means that every mention that was labeled as entity type A does indeed belong to that classification. A low precision score helps you identify places where the machine-learning annotator created incorrect annotations. The score says nothing about how many other mentions that were labeled as entity type A by the human annotator were missed by the machine-learning annotator; the recall score reflects that information. 

Recall - A measurement that specifies how many mentions that should have been annotated by a given label were actually annotated with that label - the right mentions being those that human annotators identified in the same documents. Recall is determined by the number of correctly labeled annotations divided by the number of annotations that should have been created. A recall score of 1.0 means that every mention that should have been labeled as entity type A was labeled correctly. A low recall score helps you identify places where the machine-learning annotator failed to create an annotation that it should have. The score says nothing about how many other mentions were also labeled as entity type A, but should not have been; the precision score reflects that information.

F1 score -  A measurement that considers both precision and recall to compute the score. The F1 score can be interpreted as a weighted average of the precision and recall values, where an F1 score reaches its best value at 1 and worst value at 0.

### RandomOverSampler

![ROS_acc](https://user-images.githubusercontent.com/87910875/147425757-5f961778-de24-49cd-89a9-b596e2ccb663.png)

The accuracy score for the algorithm is ~63%.

![RandomOverSampler](https://user-images.githubusercontent.com/87910875/147425246-46da2f4c-8210-4e00-ae66-3a319dcd8d03.png)

The high_risk F1 for the algorithm was 2% due to the very low precision and relatively low recall. 

### SMOTE

![SMOTE_acc](https://user-images.githubusercontent.com/87910875/147425507-b13b8500-edef-414f-9892-5c363c1d1ef4.png)

The accuracy score for the algorithm is ~63%.

![SMOTE](https://user-images.githubusercontent.com/87910875/147425875-69042602-d37f-488e-a251-e5e71f66b493.png)

The high_risk F1 for the algorithm was 2% due to the very low precision and relatively low recall of 62%. The F1 score for low_risk is decent with it being 78%.

### ClusterCentroids

![ClusterCentroid_acc](https://user-images.githubusercontent.com/87910875/147425785-e4e94c55-230c-4795-b482-5456c3ef7867.png)

The accuracy score for the algorithm is also ~63%.

![CC_acc](https://user-images.githubusercontent.com/87910875/147425784-ae3bf74b-4487-40d9-a9c9-3cf97f93651d.png)

The high_risk F1 for the algorithm was 15% due to the very low precision and relatively low recall of 59%. The F1 score for low_risk is relatively low at 60%.

### SMOTEENN

![SMOTEENN_acc](https://user-images.githubusercontent.com/87910875/147425795-b70f00f5-c029-4c6f-8657-0e33abc90372.png)

The accuracy score for the algorithm is the worst at 51%

![SMOTEENN](https://user-images.githubusercontent.com/87910875/147425794-3a9ac4bd-0b4a-4b17-a19b-35d7259b4c2f.png)

The high_risk F1 for the algorithm was 2% mostly due to the very low precision. The F1 score for low_risk is relatively low at 73%.


### BalancedRandomForestClassifier

![BalancedRandomForestClassifier_acc](https://user-images.githubusercontent.com/87910875/147425800-bcfd8187-1afc-4c22-9786-08cfdf512959.png)

The accuracy score for the algorithm is decent at 79%

![BalancedRandomForestClassifier](https://user-images.githubusercontent.com/87910875/147425801-44066cef-a2fc-4d3e-ae40-bc278cda7447.png)

The high_risk F1 for the algorithm was 6% mostly due to the very low precision. The F1 score for low_risk is very goot at 95%.



### EasyEnsembleClassifier

![EasyEnsembleClassifier_acc](https://user-images.githubusercontent.com/87910875/147425806-26b21270-f7f5-4384-b4cd-79446bfb7c74.png)

The accuracy score for the algorithm is the best at 93%

![EasyEnsembleClassifier](https://user-images.githubusercontent.com/87910875/147425805-cadbd39d-f904-4a2e-b895-caf12be55aaf.png)

The high_risk F1 for the algorithm was 15% mostly due to the very low precision. The F1 score for low_risk is very accurate at 93%.

### Summmary

I do not recommend any of the models due to relatively low accuracies for predicting credit risk. Even though the EasyEnsembleClassifier has an accuracy of 93%, I don't think it is accurate enough for predicting credit risk. If the model would be used then out of 100 loans, 7 could be inaccuarately labeled by the model and if the company is handling large quantities of loans, it could cost the company millions. 
