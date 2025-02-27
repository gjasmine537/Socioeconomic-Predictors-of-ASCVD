# Socioeconomic-Predictors-of-ASCVD
Multiple machine learning models are used in the scope of this project to predict ASCVD using socioeconomic factors.

**Abstract**

Accessing cardiovascular disease risks across different population
groups is crucial for improving healthcare treatments and tailoring
medical interventions to the specific needs of diverse communities.
This research seeks to create a predictive model to assess risk of
cardiovascular disease based on demographic factors such as gender,
ethnicity, socioeconomic status, education, etc. By processing through
medical records and public health datasets, data processing techniques
such as data cleaning, normalization, and feature selection will be used
to ensure the quality of the input data within the model. Additionally
advanced machine learning techniques such as multi-layer perceptron
(MLPs), random forests, and logistic regression will be trained to
predict outcomes and identify key risk factors for cardiovascular
diseases and hospitalization rates. After training and testing medical
and public health datasets with the model, we achieved a 89%
accuracy, demonstrating the model’s effectiveness in identifying
cardiological disease risks and predicting potential pulmonary diseases
within different population groups.

**Background**

ASCVD, or atherosclerotic cardiovascular disease, is one of the
leading causes of morbidity and mortality in the United States. This
term refers to multiple conditions in which plaque builds up in the
arteries, limiting blood flow to the rest of the body. The traditional
method of predicting a person's likelihood of developing a
cardiovascular disease focuses more on established clinical indicators
while socioeconomic risk factors remain complex and overlooked. The
features examined in this research are socioeconomic – specifically,
ethnicity, education, and income level are used as the predictors for
ASCVD. While seemly secondary, these features play a critical role in
determining one’s diet, lifestyle choices, and ability to get quality
healthcare within their communities, all of which can affect
cardiovascular health. Education can determine one’s health literacy,
which can determine the choices one make with diet and quantity of
health visits. Ethnicity can be linked to genetic predisposition as well
as cultural aspects that may affect diet and healthcare practices. The
dataset contains information about the ethnicity, income status,
education, and poverty index for each patient. We hope by using
various classification models, we can better predict future
cardiovascular disease risk based on these factors.

**Preprocessing**

Targets like income level [PIR], education [edu], ethnicity [eth], and poverty
were selected as features and were hot encoded. Missing data were filled
with the median value and data was split into two (20% testing and 80%
training) and standardization was used using standard Scaler to scale each
feature to have a mean of 0 and the standard deviation of 1. The class weight
was computed to be balanced between the positive and negative ASCVD
labels due to a much larger proportion of negative ASCVD samples.

**Classification Models**

_MLP_
• A neural network was built with the following architecture
• Input layer with matching number of the features
• Four hidden layers (dense layers 128, 64, 32 16) and an output layer early
stopping was used to avoid overfitting

_LOGISTIC REGRESSION_
• A logistic regression model was created based on a data split of 20% for
testing and 80% for training.
• Maximum iteration was set to 1000.

_RANDOM FOREST_
• A random forest model was created based on a data split of 20% for
testing and 80% for training.
• The number of estimators used was 150 and max depth was 100.
• Entropy was used to measure feature importance.

_SVM_
• SVM was created based on a data split of 20% for testing and 80% for
training,
• All kernels preformed with a difference between 2%

**Results**

_MLP_
• Leaky Relu Accuracy: 0.60

_LOGISTIC REGRESSION_
• Accuracy: 0.5717

_RANDOM FOREST_
• Accuracy: 0.6819

_SVM_
• Linear Kernel Accuracy: 0.6868
• Poly Kernel Accuracy: 0.6711
• RBF Kernel Accuracy: 0.6714
• Sigmoid Kernel Accuracy: 0.6375

**Conclusion**

Using all methods and focusing on poverty, ethnicity, and education level,
we found better results in predicting when patients did not have
cardiovascular disease than we did when estimating whether they did. By
focusing on these socio-economic factors, our prediction and hypothesis were
not heavily backed by these models, though with a more balanced dataset,
results could be promising. Further studies and sources may find that other
factors such as diet, which would need more specific data, could also be a
accurate factor of developing cardiovascular disease.

**Future Direction**

• In the future, we can add more layers to the MLP or use KNN/CNN to get
more robust data and better comparisons between different techniques.
• More people with positive ASCVD can be added to improve the models.
• This MLP model can be used by medical research companies and policy
makers to create plans to analyze and reduce the number of cardiovascular
disease diagnoses through social and economic programs.
• Additionally, the model could expand to other fields of the medicine such as
liver, respiratory, or neurological diseases.

**Acknowledgement**

We would like to thank Dr. Nouhad Rizk from the Department of Natural
Sciences and Mathematics. This work made use of open-source libraries:
Matplotlib, Numpy, Tensorflow, and Keras
