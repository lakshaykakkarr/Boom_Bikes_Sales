# Boom_Bikes_Sales

A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing 'COVID-19 pandemic'. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state. 

In such an attempt, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to COVID-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market. The company wants to know:


  - Which variables are significant in predicting the demand for shared bikes.
  - How well those variables describe the bike demands.
  - Based on various meteorological surveys and people's styles, the service provider firm has gathered a large dataset on daily bike demands across the American market based on   some factors. 


_Step 1: Data Preparation_

In the dataset it can be observed that some of the variables like 'weathersit' and 'season' have values as 1, 2, 3, 4 which have specific labels associated with them (as can be seen in the data dictionary). These numeric values associated with the labels may indicate that there is some order to them - which is actually not the case. So, we can convert such feature values into categorical string values before proceeding with model building.


Also, the column 'yr' with two values 0 and 1 indicates the years 2018 and 2019 respectively. At the first instinct, one might can think it is a good idea to drop this column as it only has two values so it might not be a value-add to the model. But in reality, since these bike-sharing systems are slowly gaining popularity, the demand for these bikes is increasing every year proving that the column 'yr' might be a good variable for prediction.


_Step 2: Model Building_

In the dataset provided it can be noticed that there are three columns named 'casual', 'registered', and 'cnt'. The variable 'casual' indicates the number casual users who have made a rental. The variable 'registered' on the other hand shows the total number of registered users who have made a booking on a given day. Finally, the 'cnt' variable indicates the total number of bike rentals, including both casual and registered. The model is to be built taking this 'cnt' as the target variable.


_Step 3: Model Evaluation_

Once done with model building and residual analysis and have made predictions on the test set, calculating the R-squared score on the test set would be a great measure to evaluate the model.

```
from sklearn.metrics import r2_score
r2_score(y_test, y_pred)
```
where y_test is the test data set for the target variable, and y_pred is the variable containing the predicted values of the target variable on the test set.
