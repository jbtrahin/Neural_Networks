# Neural_Networks
Create a deep-learning neural network to analyze and classify the success of charitable donations.

## Module Overview
In this module, we’ll explore and implement neural networks using the TensorFlow platform in Python. We’ll discuss the background and history of computational neurons as well as current implementations of neural networks as they apply to deep learning. We’ll discuss the major costs and benefits of different neural networks and compare these costs to traditional machine learning classification and regression models. Additionally, we’ll practice implementing neural networks and deep neural networks across a number of different datasets, including image, natural language, and numerical datasets. Finally, we’ll learn how to store and retrieve trained models for more robust uses.

## Project Overview
In this challenge, you’ll have to build your own machine learning model that will be able to predict the success of a venture paid by Alphabet soup. Your trained model will be used to determine the future decisions of the company.

The goals of this challenge are for you to:

1. Import, analyze, clean, and preprocess a “real-world” classification dataset.
2. Select, design, and train a binary classification model of your choosing.
3. Optimize model training and input data to achieve desired model performance.

**[Click here](https://github.com/jbtrahin/Neural_Networks/tree/master/Challenge)** to access challenge files.

## Resources

- Software: Visual Studio Code 1.39.0, Jupyter Notebook 6.0.3
- Languages: Python 3.7
- Libraries: scikit-learn 0.22.1, TensorFlow 2.0 r2.1
- Data Sources:
  1. Charity data: https://github.com/jbtrahin/Neural_Networks/blob/master/Challenge/charity_data.csv

## Analysis

### How many neurons and layers did you select for your neural network model? Why?

I picked 3 hidden layers as we have learned it is good practice to not go over three hidden layers. We know that a good rule of thumb for a basic neural network is to have two to three times the amount of neurons in the hidden layer as the number of inputs. In the first model, I had 31 inputs and went with 64 neurons (~2 times the amount of inputs). In the optimized models, I bumped the ration to 3 times the amount of inputs.

### Were you able to achieve the target model performance? What steps did you take to try and increase model performance?

On the first try, I did not reach the target predictive accuracy of 75% and capped at 70.1%.
I did 3 optimizations:
1. I increased the number of neurons from 64 to 84. Accuracy stayed the same at 70.1%.
2. I dropped the column "STATUS" as most rows had the same value (1) and changed hidden layers activation to sigmoid. Accuracy stayed the same at 70.1%.
3. I dropped the columns "STATUS", "APPLICATION_TYPE_T3", "APPLICATION_TYPE_others", "CLASSIFICATION_C1000", "CLASSIFICATION_others", "SPECIAL_CONSIDERATIONS_Y" because of the nature of the data, and ran with same parameters as 1. Accuracy went down to 69.5%.

### If you were to implement a different model to solve this classification problem, which would you choose? Why?

I would consider using a Random Forest Classifier instead of a neural network. The data would is easy to transform and fit into the requirements of this model. It would me more efficient in terms of time spent on this project.