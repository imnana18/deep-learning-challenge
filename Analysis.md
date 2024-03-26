# Deep Learning Model Performance Report

## Overview of the Analysis

In response to the requirements of the nonprofit foundation Alphabet Soup, this project aims to utilize machine learning and neural networks to develop a binary classifier. The objective is to create a tool capable of predicting the success of funding applicants, enabling Alphabet Soup to prioritize those with the highest potential for success in their ventures.

The provided dataset encompasses more than 34,000 organizations that have previously received funding from Alphabet Soup. Each organization's metadata is captured in various columns, including identification columns like EIN and NAME, as well as descriptive attributes such as APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT, and IS_SUCCESSFUL.

Through the analysis of these features, the developed binary classifier will determine whether an applicant is likely to utilize the allocated funds effectively (IS_SUCCESSFUL). This predictive tool will serve as a valuable asset for Alphabet Soup's business team, enabling them to make informed decisions regarding funding allocation and maximize the impact of their investments in nonprofit organizations.

## Results

### Data Preprocessing

- **Target Variable(s)**:
  - The target variable for the model is the IS_SUCCESSFUL column of the DataFrame.

- **Feature Variable(s)**:
  - The feature variables for the model include the remaining APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT columns.

- **Variables to be Removed**:
  - Variables that are neither targets nor features, such as NAME and EIN, should be removed from the input data.

### Compiling, Training, and Evaluating the Model

- **Model Architecture**:
  - The neural network model consists of 3 layers in total. 2 hidden layers with 128 neurons in the first input layer and 64 neurons in the second layer. We are creating a binary classifier so the final output layer has 1 neuron with 'sigmoid' activation. These numbers were chosen as part of common practice when creating neural network models that provide a moderate level of complexity for the given DataFrame. 
  - Activation functions utilized include 'relu' and 'sigmoid'.

- **Achievement of Target Performance**:
  - We were not able to acheive target performance of 75%. 
  - The model achieved 0.73 accuracy with a 0.57 loss value. it seems that the learning curve plateaus around these values even when experimenting with neuron / layer counts and column dropping or binning.

- **Steps to Improve Model Performance**:
  - Various strategies were employed to enhance model performance, including adding a third hidden layer, adjusting the activation parameter between hidden layers, adjusting neuron counts, adding 'Dropout' and 'Binary_Normalizer' functions in TensorFlow, changing value counts for binning, custom binning the 'ASK_AMT' column, and dropping the 'STATUS' and 'SPECIAL_CONSIDERATION' columns. Despite these attempts, the model plateaus around our original accuracy / loss value which indicates that the data provided is very limited for model learning.

## Summary

This model utilizes a neural network with 3 layers, including 2 hidden layers with 128 and 64 neurons respectively, to predict the success of funding applicants for Alphabet Soup. Despite efforts to optimize performance through various strategies, the model achieves an accuracy of 73%, falling short of the target of 75%, suggesting limitations in the dataset's ability to effectively inform the model's learning process. Therefore, it is recommended to explore alternative models to address this classification problem.

### Recommendation

Given the current model architecture and its performance, a recommendation for a different model to solve this classification problem could involve exploring more complex neural network architectures or alternative machine learning algorithms.

One approach would be to continue experimentation with deeper neural networks by adding additional hidden layers or increasing the number of neurons in existing layers. This increased model complexity may allow for better capture of the underlying patterns in the data, potentially improving predictive performance.

Alternatively, ensemble learning techniques such as Random Forests or Gradient Boosting Machines (GBM) could be considered. By combining the predictions of multiple base models to improve overall accuracy and generalization, we might get a clearer representation of patterns in the data and a increase accuracy.

We could also incorporate more feature engineering techniques including creating new features, transforming existing ones, or incorporating domain knowledge to enhance the model's predictive power.