1. Overview
Alphabet Soup, a nonprofit foundation, is seeking assistance in identifying the most promising funding applicants using a data-driven approach. To achieve this goal, a binary classifier will be developed using a provided dataset that contains information on over 34,000 organizations that have previously received funding from Alphabet Soup.
The objective is to predict the likelihood of success for applicants who receive funding from the foundation.

The target variable in this model was set to the 'IS_SUCCESSFUL' column.
Features:The features that were excluded 'EIN' and 'NAME', while the remaining columns were used as features.

2.Binning:
'APPLICATION_TYPE' and 'CLASSIFICATION' features had 17 and 71 distinct values, respectively, while the other features had less than 7 unique values. 
To simplify the data and facilitate analysis and modeling, a new category called 'other' was created for data values below 500 and 800 in the respective columns.

3.Compiling, Training, and Evaluating the Model

The pre-optimization model achieved a maximum accuracy of 72.8% and a loss of 55.5%. This model was built using: 'activation': 'relu', 'sigmoid',loss="binary_crossentropy", optimizer="adam"
The model is performing well in terms of accuracy, but it can still be optimized to reduce the loss further.

The optimization model underwent trials before achieving a maximum accuracy of 73.3% and a loss of 55.4%. This model was built using: {'activation': 'relu', 'tanh','sigmoid','}
Keras Tuner, a hyperparameter tuning library, was utilized during the experiments. 
Based on the results, the optimal number of epochs was found to be 35, and the activation functions were set to ['relu', 'tanh', 'sigmoid']. 
The output layer employed the "sigmoid" activation function.


3. Summary
The Results section describes the data preprocessing steps and the model building process. 
During data preprocessing, the target variable was set to 'IS_SUCCESSFUL', and various columns such as 'EIN', 'NAME'were dropped from the feature set. 
The 'APPLICATION_TYPE' and 'CLASSIFICATION' features were binned to create a new category called 'other' for data values below 500 and 800, respectively. 

Pre-optimization and optimization attempts were made to determine the optimal number of layers and the best number of epochs using Keras Tuner. 


