#Deep Learning Challenge

Overview of the Analysis:
The purpose of this was to create a deep learning model that is able to predict the success of organizations applying for funding through Alphabet Soup. This involved processing data to eliminate irrelevant features, scaling numerical data, encoding categorical data, and desiging and training a neaural network to classify organizations as successful or unsuccessful based on various features.
Results 
Data Preprocessing
Target Variable:
  - The target variable for the model is IS_SUCCESSFUL, a binary indicator of whether an   organization is successful (1) or unsuccessful (0).
Feature Variables:
- The features include the following columns (after preprocessing):
APPLICATION_TYPE (encoded)
AFFILIATION (encoded)
CLASSIFICATION (encoded)
USE_CASE (encoded)
ORGANIZATION (encoded)
STATUS (encoded)
INCOME_AMT (encoded)
SPECIAL_CONSIDERATIONS (encoded)
ASK_AMT (scaled)

Removed Variables:
EIN and NAME were removed as they are identifiers and do not provide predictive value for the target variable.


Model Structure:
The model had:
Input Layer: Matches the number of features in the scaled dataset.
First Hidden Layer: 80 neurons with ReLU activation.
Second Hidden Layer: 30 neurons with ReLU activation.
Output Layer: 1 neuron with Sigmoid activation (binary classification).
Total parameters: 5,421 (trainable).
Target Model Performance:
The model achieved:
Training Accuracy: Approximately 74%.
Validation Accuracy: Approximately 73.9%.
Test Accuracy: 72.67%.
While the model performed reasonably well, it did not reach the ideal target accuracy of 75%.
Optimization Steps:
Data Preprocessing Adjustments:
Rare categories in APPLICATION_TYPE and CLASSIFICATION were grouped into "Other" to reduce dimensionality.
Model Design Adjustments:
Tried increasing the number of neurons in the hidden layers and tested different layer architectures.
Training Adjustments:
Ran the model for 100 epochs with a batch size of 32, using 20% of the data as a validation set.
