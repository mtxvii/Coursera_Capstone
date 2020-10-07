# Coursera_Capstone


## Introduction 

Different factors such as weather, road and light conditions play an important role in traffic. The aim of this project is to analyse the impact of said factors on the severity of traffic accidents. The target audience of this analysis are governments and police as well as all road users. The outcome could help to decrease the number of accidents and make traffic safer for all participants by allowing decision makers to take measures effectively and efficiently. 

## Data 

The data set used for this analysis is provided by provided by the Seattle Department of Transportation (SDOT). It consists of 194,673 observations, and 38 variables. The dependent variable is “SEVERITYCODE”, describing the accidents’ level of severity. The aim is to identify combinations of independent variables, which lead to an increased level of severity.

The first step to achieve this goal is to clean the data, delete unrelated information, filter missing values. In the next step, variables increasing the severity shall be identified. The columns include, inter alia:

- ADDRTYPE: Address type of collision: Alley, Block, Intersection

- LIGHTCOND: The light conditions during the collision

- ROADCOND: The road condition during the collision

- SPEEDING: Speeding as a factor in the collision (Y/N)

- WEATHER: A description of the weather conditions during the time of the collision

Though “Speeding” seems to play an important role in collisions, this variable does not provide us with enough observations in our data set. I therefore decided to delete this column along with most others, and only keep weather, light condition, road condition, and address type for my analysis. 

In the next steps, I will import the data, narrow down the variables and clean the data. I will then try to see whether we can predict multiple variables’ impact on accidents’ severity.

## Methodology

After importing the dataset, I noticed that a lot of data is actually missing. The biggest loss for this analysis is most likely the variable “Speeding”. However, with 180,000 entries missing, the column is unfortunately insignificant.

I replaced all “?” to NaN and then tried to identify all missing values. I deleted columns which are not relevant for my analysis. The variables which I decided to keep are
- SEVERITYCODE
- ADDRTYPE
- PERSONCOUNT
- PEDCOUNT
- WEATHER
- ROADCOND
- LIGHTCOND

I dropped all “Unknown” values and ended up with a clean data set of 169,781 entries.

As a next step, I wanted to visualize the imbalance of “SEVERITYCODE”, as well as the impact of “LIGHTCOND” and “WEATHER” on the severity levels of traffic accidents.

In preparation for the next steps, I got dummy variables for all categorical entries and balanced the data set to achieve a non-biased model.

Finally, I set the test and train data set for a logistic regression, as the dependent variable is binary.

## Results

Surprisingly, most accidents happen during clear weather. The model chosen to analyse the data is able to predict the severity of accident with 63% accuracy based on the test data.

## Discussion

The data set included categorical data which had to be transformed to numerical values. Moreover, the data set was unbalanced which had to be addressed by undersampling the dependent variable randomly.

As already mentioned above, the variable “SPEEDING” would have been useful for the analysis. However, too many entries were missing.

## Conclusion

Logistic regression gives a decent accuracy in predicting severity of accidents. The information retrieved from this analysis could be useful for governments, automotive manufacturers, insurance companies and most of all vulnerable road users.
