# deep-learning-challenge

## Overview of the Analysis

* The purpose here is to analyze a dataset from a nonprofit foundation called 'Alphabet Soup' that wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. 


## Results

* Data Preprocessing:

  * Target variable: 
  
  **IS_SUCCESSFUL** — Was the money used effectively

  * Features variables: 

    **APPLICATION_TYPE** — Alphabet Soup application type

    **AFFILIATION** — Affiliated sector of industry

    **CLASSIFICATION** — Government organization classification

    **USE_CASE** — Use case for funding

    **ORGANIZATION** — Organization type

    **STATUS** — Active status

    **INCOME_AMT** — Income classification

    **SPECIAL_CONSIDERATIONS** — Special considerations for application

    **ASK_AMT** — Funding amount requested

  * Variables removed from the input data because they are neither targets nor features: 
  
  **EIN and NAME** — Identification columns


* Compiling, Training, and Evaluating the Model:

  * I've started the model randomly selecting 100 neurons for the first layer and 50 neurons for the second hidden layer. Also, I've chosen the ReLU activation function for the first and second hidden layer due to the multiple results property of the function. As for the output layer, that's a binary decision of either approve or not approve an applicant for funding, therefore, I used the Sigmoid activation function.

  * After 4 iterations, the models were not able to achieve the 75% target model performance. The closest accuracy performance achieved was 68% when I've increased the number of neurons in the first layer to 200 and the second hidden layer to 100 neurons.

  * In order to optimize the model performance, I've randomly tried to:

    1. Increase the number of neurons to 200 in the first layer and 100 for the second hidden layer, achieving 68% accuracy performance. 
        In a second attempt, I've decreased the number of epochs since the accuracy levels off at the 11 epochs iteration in the previous attempt, achieving 53% accuracy performance. 

    2. Besides increasing the number neurons, I've added one more layer, keeping the epoch number to 150 iterations, achieving 57% accuracy performance. 

    3. Besides increasing the number neurons and layers, I've increased the epoch number to 300 iterations, achieving 55% accuracy performance.
    

## Summary

* Although the deep learning models were not able to achieve the 75% target model performance, my recommendation would be to use the 'First Try Model' as its achieved 68% of accuracy performance. This model used 200 neurons in the first layer and 100 in the second hidden layer. It had two hidden layers and ReLU activation function for the first and second hidden layer. Finally, it used 150 epochs iterations. 

* However, if we examine other classification models that could solve this binary problem (either approve or not approve an applicant for funding), we have to consider that other supervised learning models such as Logistic Regression, Support Vector Machines and Decision Trees could have been used here and, perhaps, have a better performance.
Counterintuitively, I've provided more resources to the deep learning models in the dataset analysis above and yet the accuracy performance did not improve, but decreased.  
Therefore, if we take into account the deep learning 'Black Box problem', where we are unable to understand the deep learning models decision making process reasoning, it becomes self-evident that the supervised learning models are the best choice for this analysis.