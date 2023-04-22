# MLB Hitting Analysis
**Explore and analyze the hitting data of Major League Baseball (MLB) players.**

![](./Images/mlb.png)

The purpose of this analysis is to provide insights into the factors that contribute to a player's batting success. By examining various statistical measures, such as batting average, slugging percentage, and on-base percentage, the analysis aims to identify the key indicators of a player's hitting performance.

This analysis can be valuable for baseball fans, coaches, and analysts who are interested in understanding the factors that contribute to a player's batting performance. The insights from this analysis can also be used to inform player scouting, player development, and game strategy.

The Jupyter Notebook is written in Python and uses various data analysis and visualization libraries such as Pandas, Matplotlib, and Seaborn. The analysis is presented with detailed explanations of the methodology and findings.

This repository can be a valuable resource for anyone interested in data analysis, baseball, or both. It can be easily forked and customized for further analysis or adapted to other sports and domains.

---

## Data

The dataset on all-time baseball hitting and pitching provides a comprehensive collection of historical performance data in Major League Baseball (MLB). It includes batting statistics such as hits, home runs, batting average, and RBIs, and pitching statistics such as earned run average (ERA), strikeouts, and wins. The data spans from the early days of MLB in the late 1800s to the present day, making it a valuable resource for researchers and baseball enthusiasts alike.

The dataset offers opportunities to study the evolution of baseball over time, from changes in playing styles and rules to advancements in equipment and training methods. It also enables researchers to examine the performances of individual players and teams across different eras, allowing for comparisons and analyses of different eras in baseball history.

Overall, this dataset is a valuable resource for anyone interested in baseball history and statistics, and provides a foundation for further research and analysis in the field.


The data file named "baseball_hitting.csv" contains information on the hitting statistics of baseball players, with each row representing a player's performance in a specific season. The columns in the dataset are as follows:

Player name: The name of the player.
Position: The player's position in the field, such as outfielder, catcher, etc.
Games: The number of games in which the player participated.
At-bat: The number of times the player was at-bat.
Runs: The number of runs scored by the player.
Hit:The number of hits achieved by the player.
Double (2B): The number of doubles hit by the player.
Third baseman (3B): The number of triples hit by the player.
Home run: The number of home runs hit by the player.
Run batted in (RBI): The number of runs batted in by the player.
A walk: The number of times the player received a walk.
Strikeouts: The number of times the player struck out.
Stolen base: The number of stolen bases achieved by the player.
Caught stealing: The number of times the player was caught stealing a base.
AVG: The player's batting average, calculated as the ratio of hits to at-bats.
On-base percentage (OBP): The percentage of times the player reaches base, calculated as the sum of hits, walks, and hit-by-pitches divided by the sum of at-bats, walks, hit-by-pitches, and sacrifice flies.
Slugging percentage (SLG): A measure of the player's power at the plate, calculated as the total number of bases achieved divided by the total number of at-bats.
On-base plus slugging (OPS): The sum of the player's on-base percentage and slugging percentage, a measure of the player's overall offensive performance.

---

## Analysis
The Jupyter Notebook file contains a step-by-step analysis of the hitting data, including data cleaning, feature engineering, and exploratory data analysis. Various statistical techniques are applied to the data to gain insights into the performance of MLB hitters.

**Data Cleaning:** The first step in the analysis was to clean the dataset. This involved removing any duplicate or irrelevant data and ensuring that all data was formatted correctly. The dataset contained missing values, so we had to decide how to handle these missing values. In this analysis, we chose to remove any rows with missing values, as this was the most appropriate method for this particular dataset.

- The first step in any data analysis is to clean the dataset. This involves removing any duplicate or irrelevant data and ensuring that all data is formatted correctly.

- In this analysis, we loaded the "baseball_hitting.csv" file into a pandas DataFrame using the read_csv function.

- We checked the shape of the DataFrame to get a sense of how many records and columns we are working with.

- We used the info() method to check the data types of each column and to see if there are any missing values.

- We noticed that there were missing values in some of the columns. We decided to remove any rows with missing values, as this was the most appropriate method for this particular dataset.

- We also removed any rows with invalid data, such as negative values for hits, at-bats, or plate appearances.

**Exploratory Data Analysis:** 

- After cleaning the data, we conducted an exploratory data analysis (EDA) to gain a better understanding of the variables in the dataset.

- We used various visualization techniques such as histograms, scatterplots, and box plots to identify any patterns or outliers in the data.

- We plotted the distribution of each variable to see how they are distributed and if there are any outliers or anomalies.

- We also created scatterplots to explore the relationship between variables, such as the relationship between a player's batting average and their number of hits or plate appearances.

- We used box plots to identify any differences in performance between different player positions or different years.

**Feature Engineering:** 

- The next step in the analysis was to engineer new features from the existing dataset. We created new variables that we thought might be useful in predicting the target variable (in this case, a player's batting average).

- We created a new column called "age" by subtracting a player's birth year from the year of the season.

- We also created a new column called "hits_per_plate_appearance" by dividing a player's total number of hits by their total number of plate appearances.

- These new features could potentially provide additional information that might be useful in predicting a player's batting average.

**Modeling:**

- With the dataset cleaned, explored, and engineered, we moved on to building predictive models.

- In this analysis, we used two different models: a linear regression model and a random forest model.

- We split the dataset into training and testing sets using the train_test_split function from scikit-learn.

- We trained the linear regression model on the training data and used it to make predictions on the testing data. We evaluated the model's performance using mean squared error (MSE) and R-squared (R2).

- We also trained a random forest model on the training data and used it to make predictions on the testing data. We evaluated the model's performance using mean squared error (MSE) and mean absolute error (MAE).

**Model Evaluation:** 

- Finally, we evaluated the models based on their performance metrics.

- For the linear regression model, we calculated the mean squared error (MSE) and R-squared (R2) on the testing data.

- For the random forest model, we calculated the mean squared error (MSE) and mean absolute error (MAE) on the testing data.

- We compared the performance of both models and chose the one that performed better for predicting a player's batting average.

- We also looked at the feature importances of the random forest model to see which features were most important in predicting the target variable.

- After evaluating both models, we found that the random forest model performed better than the linear regression model.

- The random forest model had a lower MSE and MAE on the testing data, indicating that it was better at predicting a player's batting average.

- Additionally, the feature importances of the random forest model showed that the most important features were the player's on-base percentage, slugging percentage, and number of home runs.

- We can use this information to make recommendations to coaches and managers on how to improve a player's batting average. For example, if a player has a low on-base percentage, coaches could work with them on improving their plate discipline and increasing their walks. If a player has a low slugging percentage, coaches could work with them on hitting for more power and extra-base hits.

- Overall, our model provides a useful tool for predicting a player's batting average and identifying areas for improvement in their performance.

---

## Requirements
To run the Jupyter Notebook file, the following Python libraries are required:


    pandas
    numpy
    matplotlib
    seaborn
    scipy
    These libraries can be installed using pip, a Python package installer.

---

## Usage
To run the Jupyter Notebook file:

- First, ensure that the required Python libraries are installed. 

- Next, clone this repository to your local machine and open the BaseballHittingAnalysis.ipynb file in a Jupyter Notebook environment. 

- From here, you can execute the cells of the notebook to reproduce the analysis.

---

## Conclusion

Through this analysis, we were able to identify several factors that contribute to a player's hitting success in Major League Baseball. We found that a player's number of hits, number of plate appearances were significant predictors of their batting average.

We also found that the random forest model outperformed the linear regression model in predicting a player's batting average. The random forest model had a lower mean squared error and mean absolute error, indicating that it was better able to capture the variance in the data.

Overall, this analysis provides valuable insights into the factors that contribute to a player's hitting performance in baseball. The findings can be used to inform player scouting, player development, and game strategy, and can also serve as a foundation for further research in the field.

---

## Author
This analysis was performed by Richie Garafola, a data science enthusiast and baseball fan.