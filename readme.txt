Abstract:
In this competition, you’ll develop accurate models of metered building energy usage in the following areas: chilled water, electric, hot water, and steam meters. The data comes from over 1,000 buildings over a three-year timeframe. With better estimates of these energy-saving investments, large scale investors and financial institutions will be more inclined to invest in this area to enable progress in building efficiencies.
***first visualisation:
we have 5 dataframes:
Size of train_df data (20216100, 4)
Size of weather_train_df data (139773, 9)
Size of weather_test_df data (277243, 9)
Size of building_df data (1449, 6)
Size of test_df data (41697600, 4)
we need to concat différents data to get a modéle
primary_use the feature of building_df is a string with limited value
****Reducing size
to have a quickly running modele we need this function
****feature engineering 1:
returning the primary_use to category type 
*****Merging dataframes
******Visualisation
the size of the train_df is (20216100, 16)
the size of the test_df is (41697600, 16)
we have very noisy features for example :year_built,floor_count,cloud_coverage ..
correlation matrix:square_feet,floor_count,air_temperature,dew_temperature 
****Data cleaning:
filling missing values floor_count,win_speed.... 
drop wind_direction, dew_temperature,precip_depth_1_hr,sea_level_pressure because they have many missing values and their correlation with target is baisses
*feature engineering:
label encoding for primary_use because it is a category ordred
timestamps-->d-m
square feet is asymetric --> log
delete timestamp 
****data preparation evaluation
the types of columns are int/float
the sum of missing values is 0
***modeling
separtion train_df 0.7/0.3
lstm
***
