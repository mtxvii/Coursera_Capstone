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
