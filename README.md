**Report For Deep Learning Challenge**
Overview
    In this assignment, we analyzed data of the thousands of companies Alphabet Soup has invested in over the years and their success so that the company might have a tool to make better funding decisions moving forward. We created this tool by leveraging a machine learning model - teaching it how to identify if a company would be successful or not. It did this by analyzing the "features" (variables associated with each company that received investment) without viewing the information labeling each company as successful or not, then checking its accuracy against that information. With this model, Alphabet Soup will have one more tool to help determine whether or not they should invest in a new company.
 
Results:
    Using bulleted lists and images to support your answers, address the following questions:

Data Preprocessing
    What variable(s) are the target(s) for your model?
        * The target variable is the binary successful or not successful rating of each company in the data set.
    What variable(s) are the features for your model?
        * The features of the data set are the other variables under consideration: application type, affiliation, classification, use case, organization, status, income amount, special considerations, and ask amount.
    What variable(s) should be removed from the input data because they are neither targets nor features?
        * EIN and Name were removed from the data set because they do not have a meaningful effect on the success of the company and therefore are neither features nor targets. 

Compiling, Training, and Evaluating the Model
    How many neurons, layers, and activation functions did you select for your neural network model, and why?
        * I used two layers because that is the standard number of layers, and adding more did not improve accuracy. Two layers is typically enough to train the model without increasing runtime unnecessarily.
        * I selected 80 neurons for the first layer and 30 neurons for the second layer because reducing the number of neurons improved accuracy. Typically increasing neurons has a diminishing rate of returns, but reducing them increased my accuracy indicating there may have been an over fitting issue.
        * For the activation functions, I used ReLU, rectified linear unit, because it was specified in our assignment, and is typically a good option when needing to introduce non-linearity to the model. It is also simple and effective in hidden layers.
    Were you able to achieve the target model performance?
        * No, I was not.
    What steps did you take in your attempts to increase model performance?
        * Start accuracy: 72.51%
        * First, I increased filtering to limit the amount of data being processed. Accuracy: 72.26%
        * Then, I decreased the filtering. Accuracy: 72.63%
        * Decreased filtering further: 72.54%
        * Set filtering to best so far. Increased number of neurons: 72.41%
        * Decreased number of neurons: 72.68%
        * Increased number of hidden layers with same max neurons: 72.31%
        * Decreased hidden layers and neurons: 72.55%


Summary:

The Alphabet Soup challenge aimed to create a machine learning model that oculd predict the success of a company receiving funding. To create this model, I first processed and cleaned the data to identify the characteristics of the data set and limit what the model processed during its learning, including removing erroneous information and binning rare occurences. Once the data was ready, I ran it through the machine learning model and tested its accuracy.

The goal was to create a model with 75% accuracy. I was only able to generate 72.68% accuracy after attempts to adjust the layers, neurons, and data. There is clearly room for improvement in this model. A different approach may be necessary. Gradient Boosting Classifiers may be helpful. I did some research on them, and it appears that they can assign weights to different variables, making them especially effective at classifying items to categories (is company x most likely going to be successful or unsuccessful). Having the model identify the importance of features could also help human decision makers in their own decision process.
