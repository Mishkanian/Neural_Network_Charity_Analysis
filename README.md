# Neural Network Charity Analysis

## Project Overview
The purpose of this project is to create a a binary classifier that is capable of predicting whether applicants will be successful if funded by a fictional company "Alphabet Soup." After the data is preprocessed, a Neurnal Network Model is compiled, trained and evaluated. Finally, there is an attempt made to optimize the model by increasing the accuracy to 75% or higher.

## Software and Resources

- Python 3.7
- pandas 1.2.4
- sklearn 0.24.1
- tensorflow 2.5.0

- Data: [charity_data.csv](https://github.com/Mishkanian/Neural_Network_Charity_Analysis/blob/main/Resources/charity_data.csv)

## Results


### Data Preprocessing

After reading in the [charity_data.csv](https://github.com/Mishkanian/Neural_Network_Charity_Analysis/blob/main/Resources/charity_data.csv) file to a Pandas DataFrame, the "EIN" and "NAME" columns were dropped from the dataset. These identification columns did not contain any valuable information. 

Columns with more than 10 unique values, such as the "CLASSIFICATION" and "APPLICATION_TYPE" columns, have had their rare categorical variables binned into a new "other" column. A list of categorical variables is generated and is then encoded using OneHotEncoder. These encoded variable names are added to a new dataframe. After merging the one-hot encoded features, the originals are dropped.

The variable considered the target for this model is "IS_SUCCESSFUL," all other variables in the dataframe are considered features. The numerical variables are standardized using Scikit-Learn’s StandardScaler module.

### Compiling, Training, and Evaluating the Model

![original_accuracy](https://github.com/Mishkanian/Neural_Network_Charity_Analysis/blob/main/README_Images/accuracy_original.png)

#### Optimization Attempt 1

![attempt1](https://github.com/Mishkanian/Neural_Network_Charity_Analysis/blob/main/README_Images/attempt1_accuracy.png)

In the first attempt to optimize this model, the number of neurons in the hidden layers were increased.

#### Optimization Attempt 2

![attempt2](https://github.com/Mishkanian/Neural_Network_Charity_Analysis/blob/main/README_Images/attempt2_third_layer_accuracy.png)

In the second attempt, a third hidden layer was added to the model with 4 neurons

#### Optimization Attempt 3

![attempt3](https://github.com/Mishkanian/Neural_Network_Charity_Analysis/blob/main/README_Images/attempt3_tanh.png)


## Summary

[PROJECT IN PROGRESS]


**Author: Michael Mishkanian**  
For all questions and inquiries, please contact me on [LinkedIn](https://www.linkedin.com/in/michaelmishkanian/).
