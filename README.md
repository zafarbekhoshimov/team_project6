# team_project6
## Household electirc power consumption
This project contains 2075259 measurements gathered in a house located in Sceaux (7km of Paris, France) between December 2006 and November 2010 (47 months).

## Data
1. The expression (global_active_power * 1000 / 60 - sub_metering_1 - sub_metering_2 - sub_metering_3) calculates the amount of active energy consumed per minute in watt-hours by electrical devices in the household that are not covered by sub-meterings 1, 2, or 3.
2. In the dataset, there are some instances where the measurements are missing, accounting for roughly 1.25% of the rows. While all calendar timestamps are present, certain timestamps lack measurement values.
   A missing value is indicated by the absence of data between two consecutive semicolon attribute separators. For example, there are missing values on April 28, 2007.

## Model
Model in this project is developed using deep learning optimimzers in tensorflow. As dataset a date-time type we used date-time as its indexes. Although the amount of energy consumed is calculated per minute, we first resampeld it into hours as there was too much information,
even after resampling it into hours it took quite bit of time. So, in the second part we resampled it into days. After resampling it into days our models started training faster as there were a lot less data. We trained our models by resampling them into hours and then into days.

## Evaluation
The performance of our models is evaluated using metrics such as rmse(root_mean_squared_error), mse(mean_squared_error), mae(mean_absolute_error). 

