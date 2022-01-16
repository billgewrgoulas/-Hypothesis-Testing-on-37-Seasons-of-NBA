# Hypothesis Testing on 37 Seasons of NBA

## Introduction

The purpose of this project is to analyze the NBA statistics Dataset from Kaggle and extract usefull information by applying various statistical analysis and hypothesis testing methods.

## Objectives

* Apply data pre-processing on the Data
* Extract usefull conclusions by creating various plots of the Data
* Apply hypothesis testing methods.

<img src='https://github.com/KGharib/Test-Gif/blob/master/Lebron.gif'>

## Part 1 Statistical Analysis

#### Step 1 - Data Pre-Processing
* Keep only seasons from 1980 to 2017.
* Keep only the players of age 18 to 40 years old.
* Focus only on the main positions PG, SG, SF, PF, C.

#### Step 2 - Create the hist plots of the points of each player per season.
* We observe that the points of the players follow the chi-squere distribution.
* Use the log-scale method to better visualize the plots.

#### Step 3 Analyze how age affects player performance.
* For each player calculate the metrics: PPG, APG, BPG, TS%, PER, RPG for each season.
* Create a line plot for each metric.
* Observe that the age factor has a direct correlation with player performance and affects each metric differently.

#### Step 4 Analyze if player performance with the age is affected by the position.
* Create lineplots for the metrics using the position as the grouping variable
* Observe that there is a correlation between the player performance metrics and the age and position.
* Some metrics in certain positions are affected more as time passes.

#### Step 5 In this step we are interested in investigating whether there is a correlation between the metrics PPG, APG, RPG, BPG.
* Calculate the statistics for each player but using the data from all the seasons the player has participated.
* Create the scatter plots for all pairs of the metrics in order to find any linear relationships.
* To extract more accurate results perform the <b>Pearson Correlation Test</b> on the Data.
* From the results of the test we can tell that there are statistical significant relationsips between the metrics.
* Do the same for the positions and extract more specific correlations.

#### Step 6 In this part we want to study if there is a difference between the performance of players who play in a different position.
* Use the metrics from the previous step and create barplots with the average values for different positions, with 95% -confidence intervals.
* Observe that the players perform differntly when playing in different positions.

## Part 2 Hypothesis Testing

#### Question 1 In this part we want to find which position is the best for a player, by studying the PER metric in different positions.
* First create the corresponding barplot PER-Position similary to step 6.
* Observe that all positions seem equal in terms of Player Efficiency Rate.
* In order to decide which position is the most efficient we will make the following assumptions:
*  -H0 Null hypothesis: There is no significant difference between the PER in different positions.
*  -H1 Alternate hypothesis: There is significant difference between the PER in different positions.
* Using the <b>Student T-Test</b> we conclude that there are some significant differences of the means in different positions.

#### Question 2 In this part we will focus our attention on player Russell Westbrook, who has achieved a significant number of Triple-Doubles.
* First using the data we will find the chance of his team winning when he has achieved triple-double is and compare it to the probability of his team winning regardless if he has achiaved a tripple double, in order to understand if this is beneficial for his team.
* Subsequently we will assume the following:
*  -H0: There is no dependence between a victory and the triple-double Of Russel
*  -H1: There is a correlation between a victory and the triple-double Of Russel
* In this case we will apply the <b>Chi-Squere Test of Independence</b> to test the Hypothesis.
* From the results we find that the H0 is rejected thus there is correlation between a victory and the triple-doubles Of Russel.

#### Question 3 In this part we will study if there is a correlation between the number of assists peripheral players give to one team (the backcourt - PG, SG) and the points scored by the tall ones in the team (the frontcourt - SF, PF).
* To test this we are going to use the <b> Pearson Correlation Coefficient</b>.
* First we will calculate the observations for each team and for each Season and then apply the test.
* From the results we can conclude that there is positive linear relationship between the metrics with coefficient = 0.58.

#### Question 4 In this part we will find out if teams score an average of more points at home vs away.
* We will examine the teams: Boston Celtics and Minnesota Timberwolves and assume the following:
*  -H0: There is no significant difference between points at home vs away.
*  -H1: There is a significant difference between points at home vs away.
* In order to test these assumptions we will perform two experiments:
* First we will use the <b>Student T-Test</b> and afterwords we will do a <b>permutation test</b>
* From the results of the two tests we can reject the H0 for Boston Celtics but not for Minnesota Timberwolves.

