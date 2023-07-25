The purpose of this analysis is to deploy a neural network on data from a nonprofit foundation, in order to help the nonprofit select the applicants for funding. Specifically, we created a binary classifier to predict whether applicants will be successful if funded by the nonprofit.

The source data is a CSV containing more than 34,000 organizations that have received funding and a number of columns that capture metadata about each organization, such as:

EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special considerations for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively

### Data Preprocessing

The target variable is 'IS_SUCCESSFUL', as we wish to predict whether an applicant will use its grant money effectively. All other metadata is included in the feature variables, with the exception of unique identifiers (i.e., EIN and name), irrelevant variables (i.e., STATUS), and variables with excessive outliers (i.e., SPECIAL_CONSIDERATIONS). 

### Compiling, Training, and Evaluating the Model

Our model consists of 2 layers, each with 16 neurons, and a relu activation function.

We were unable to achieve target model performance of 75% or higher, despite various attempts to increase model performance. These include additional binning of features, re-insertion of the STATUS and SPECIAL_CONSIDERATIONS columns, and adjustments to the model parameters (e.g., number of layers, number of neurons, and different activation functions). 

On test data, the model exhibited accuracy of 73% of loss of over 55%. Given its lack of precision and recall, we do not recommend this model, and would instead recommend exploring alternate models for this classification problem. Logistic regression would be a natural choice given its track record of performance in classification problems with categorical data.  
