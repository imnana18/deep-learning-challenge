# Deep Learning Charity Prediction Model

## Introduction

In response to the requirements of the nonprofit foundation Alphabet Soup, this project aimed to develop a binary classification model using machine learning and neural networks. The objective was to create a tool capable of predicting the success of funding applicants, aiding Alphabet Soup in selecting organizations with the highest potential for success in their ventures.

## Assignment Map

📁 `Saved_Models`

 - `AlphabetSoupCharity.h5`: saved model for initial model training and testing.
 - `AlphabetSoupCharity_Optimization.h5`: saved model for optimization training and testing.

📁 `Unsolved`

 - `AlphabetSoupCharity.ipynb`: code for processing data and initial neural network training-testing.
 - `AlphabetSoupCharity_Optimization.ipynb`: code for processing data in attempts to optimize neural network model.
 - 📊 `Analysis.md`: written report on the neural network model.


## Files

The necessary files were downloaded from the following link: [Module 20 Challenge files]((https://static.bc-edx.com/data/dl-1-2/m20/lms/starter/Starter_Code.zip)).

## Overview of the Assignment

1. **Data Preprocessing**: 
    - The provided dataset, containing information on over 34,000 organizations funded by Alphabet Soup, was preprocessed using `Pandas` and `scikit-learn's StandardScaler()`. This step involved identifying target and feature variables, dropping irrelevant columns, encoding categorical variables, and splitting the data into training and testing datasets.

2. **Model Development**:
    - A `neural network model` was designed using `TensorFlow` and `Keras` to create a binary classification model. The model architecture included input, hidden, and output layers, with appropriate activation functions chosen. The model was compiled, trained, and evaluated to calculate `loss` and `accuracy`.

3. **Model Optimization**:
    - Various methods were employed to optimize the model's predictive accuracy in attempt to reach `75% accuracy`. This included adjusting input data, modifying the neural network architecture by adding `neurons` or `layers`, using different `activation functions`, and altering training `epochs`.

4. **Report Writing**:
    - A comprehensive report was written to document the analysis process and results. The report provided an overview of the analysis, details on data preprocessing, model architecture, training, evaluation, and optimization steps, as well as a summary of overall findings and recommendations for further improvements.

## Conclusion

Through this assignment, a deep learning model was developed to predict the success of funding applicants for Alphabet Soup. While the model achieved moderate success in prediction accuracy, further optimization and exploration of alternative model architectures and feature engineering techniques could enhance its performance. Overall, the assignment provided valuable insights into the application of machine learning and neural networks in addressing real-world challenges faced by nonprofit organizations.

 
