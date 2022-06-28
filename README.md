# SpaceX-Falcon9-DataScience-Capstone
#  INTRODUCTION

![starlink-launch-3-18](https://user-images.githubusercontent.com/100082194/176105487-ffdc53e9-0772-4614-95da-8962766bc0b3.gif)

 
 In this capstone, we will predict if the Falcon 9 first stage will land successfully. SpaceX advertises Falcon 9 rocket launches on its website, with a cost of 62 million dollars; other providers cost upward of 165 million dollars each, much of the savings is because SpaceX can reuse the first stage. Therefore if we can determine if the first stage will land, we can determine the cost of a launch. This information can be used if an alternate company wants to bid against SpaceX for a rocket launch.

This capstone project course will give you a taste of what data scientists go through in real life when working with real datasets. You will assume the role of a Data Scientist working for a startup intending to compete with SpaceX, and in the process follow the Data Science methodology involving data collection, data wrangling, exploratory data analysis, data visualization, model development, model evaluation, and reporting your results to stakeholders. You are tasked with predicting if the first stage of the SpaceX Falcon 9 rocket will land successfully.

# Problem to determine
SpaceX advertises Falcon 9 rocket launches on its website, with a cost of 62 million dollars; other providers cost upward of 165 million dollars each, much of the savings is because SpaceX can reuse the first stage. Therefore if you can accurately predict the likelihood of the first stage rocket landing successfully, you can determine the cost of a launch. With the help of your Data Science findings and models, the competing startup you have been hired by can make more informed bids against SpaceX for a rocket launch.

# step by step process

 1- [COLLECTING DATA](https://github.com/ilaki-prog/SpaceX-Falcon9-DataScience-Capstone/blob/main/Space%20X%20Data%20collection.ipynb)
 
 Task 1: Request and parse the SpaceX launch data using the GET request
 
 Task 2: Filter the dataframe to only include Falcon 9 launches
 
 Data Wrangling
 
 Task 3: Dealing with Missing Values
 
 2- [DATA COLLECTION WITH WEB SCRAPING](https://github.com/ilaki-prog/SpaceX-Falcon9-DataScience-Capstone/blob/main/Data%20Collection%20with%20web%20scraping%20(1).ipynb)
 
 
Web scrap Falcon 9 launch records with BeautifulSoup:

Extract a Falcon 9 launch records HTML table from Wikipedia
Parse the table and convert it into a Pandas data frame

TASK 1: Request the Falcon9 Launch Wiki page from its URL

TASK 2: Extract all column/variable names from the HTML table header

TASK 3: Create a data frame by parsing the launch HTML tables


3-[DATA WRANGLING](https://github.com/ilaki-prog/SpaceX-Falcon9-DataScience-Capstone/blob/main/EDA.ipynb)

Data Analysis

TASK 1: Calculate the number of launches on each site

TASK 2: Calculate the number and occurrence of each orbit

TASK 3: Calculate the number and occurence of mission outcome per orbit type

TASK 4: Create a landing outcome label from Outcome column

4 - [EDA WITH DATA VISUALIZATION](https://github.com/ilaki-prog/SpaceX-Falcon9-DataScience-Capstone/blob/main/eda-%20Visualization.ipynb)

TASK 1: Visualize the relationship between Flight Number and Launch Site

TASK 2: Visualize the relationship between Payload and Launch Site

TASK 3: Visualize the relationship between success rate of each orbit type

TASK 4: Visualize the relationship between FlightNumber and Orbit type

TASK 5: Visualize the relationship between Payload and Orbit type

TASK 6: Visualize the launch success yearly trend

Features Engineering

TASK 7: Create dummy variables to categorical columns

TASK 8: Cast all numeric columns to float64

5-[EDA WITH SQL](https://github.com/ilaki-prog/SpaceX-Falcon9-DataScience-Capstone/blob/main/EDA%20with%20SQL.ipynb)

Understand the Spacex DataSet
Load the dataset into the corresponding table in a Db2 database
Execute SQL queries to answer assignment questions
Overview of the DataSet
SpaceX has gained worldwide attention for a series of historic milestones.

It is the only private company ever to return a spacecraft from low-earth orbit, which it first accomplished in December 2010. SpaceX advertises Falcon 9 rocket launches on its website with a cost of 62 million dollars wheras other providers cost upward of 165 million dollars each, much of the savings is because Space X can reuse the first stage.

Therefore if we can determine if the first stage will land, we can determine the cost of a launch.

This information can be used if an alternate company wants to bid against SpaceX for a rocket launch.

This dataset includes a record for each payload carried during a SpaceX mission into outer space.

Connect to the database

Task 1
Display the names of the unique launch sites in the space mission

Task 2
Display 5 records where launch sites begin with the string 'CCA'

Task 3
Display the total payload mass carried by boosters launched by NASA (CRS)

Task 4
Display average payload mass carried by booster version F9 v1.1

Task 5
List the date when the first successful landing outcome in ground pad was acheived.

Task 6
List the names of the boosters which have success in drone ship and have payload mass greater than 4000 but less than 6000

Task 7
List the total number of successful and failure mission outcomes

Task 8
List the names of the booster_versions which have carried the maximum payload mass. Use a subquery

Task 9
List the failed landing_outcomes in drone ship, their booster versions, and launch site names for in year 2015


Task 10
Rank the count of landing outcomes (such as Failure (drone ship) or Success (ground pad)) between the date 2010-06-04 and 2017-03-20, in descending order

6-[LAUNCH SITES LOCATION ANALYSIS WITH FOLIUM](https://github.com/ilaki-prog/SpaceX-Falcon9-DataScience-Capstone/blob/main/Launch%20Sites%20Locations%20Analysis%20with%20Folium.ipynb)

The launch success rate may depend on many factors such as payload mass, orbit type, and so on. It may also depend on the location and proximities of a launch site, i.e., the initial position of rocket trajectories. Finding an optimal location for building a launch site certainly involves many factors and hopefully we could discover some of the factors by analyzing the existing launch site locations.

Task 1: Mark all launch sites on a map

Task 2: Mark the success/failed launches for each site on the map

TASK 3: Calculate the distances between a launch site to its proximities

7-[MACHINE LEARNING PREDICTION](https://github.com/ilaki-prog/SpaceX-Falcon9-DataScience-Capstone/blob/main/Space%20X%20Machine%20Learning%20Prediction.ipynb)

Perform exploratory Data Analysis and determine Training Labels

create a column for the class
Standardize the data
Split into training data and test data
-Find best Hyperparameter for SVM, Classification Trees and Logistic Regression

Find the method performs best using test data

Load the dataframe

TASK 1
Create a NumPy array from the column Class in data, by applying the method to_numpy() then assign it to the variable Y,make sure the output is a Pandas series (only one bracket df['name of column']).

TASK 2
Standardize the data in X then reassign it to the variable X using the transform provided below.

TASK 3
Use the function train_test_split to split the data X and Y into training and test data. Set the parameter test_size to 0.2 and random_state to 2. The training data and test data should be assigned to the following labels.

X_train, X_test, Y_train, Y_test

TASK 4
Create a logistic regression object then create a GridSearchCV object logreg_cv with cv = 10. Fit the object to find the best parameters from the dictionary parameters

TASK 5
Calculate the accuracy on the test data using the method score:

TASK 6
Create a support vector machine object then create a GridSearchCV object svm_cv with cv - 10. Fit the object to find the best parameters from the dictionary parameters.

TASK 7
Calculate the accuracy on the test data using the method score:

TASK 8
Create a decision tree classifier object then create a GridSearchCV object tree_cv with cv = 10. Fit the object to find the best parameters from the dictionary parameters.

TASK 9
Calculate the accuracy of tree_cv on the test data using the method score:

TASK 10
Create a k nearest neighbors object then create a GridSearchCV object knn_cv with cv = 10. Fit the object to find the best parameters from the dictionary parameters.

TASK 11
Calculate the accuracy of tree_cv on the test data using the method score:

TASK 12
Find the method performs best:



ouptuts for all the Tasks are given above in the Notebook


# RESULT

The exploratory data analysis has shown us that successful landing outcomes are somewhat correlated with flight number. It was also apparent that successful landing outcomes have had a significant increase since the year 2015.
All launch sites are located near the coast line. Perhaps, this makes it easier to test rocket landings in the water.
sites are also located near highways and railways. This may facilitate transportation of equipment and research material.
The machine learning were able to predict the landing success of rockets with an accuracy score of 83.33%.

