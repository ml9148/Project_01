# Project Title: Player Trends of the Chicago Cubs Across the Years

## Team Members: Project Group 2
- Emily Bowers
- Joe Cotten
- Amanda Dunaway
- Luis Martinez
- Carlie Rhoads


## Description of the Data 
The driving purpose of this project is to examine comprehensive data and determine trends across players of the Major League Baseball team, the Chicago Cubs. We have access to pitching and batting statistics, and will be looking at trends such as if age has an impact on factors such as runs batted or runs allowed.


Chicago Cubs Batting & Pitching (1876-2023) – [downloaded from Kaggle](https://www.kaggle.com/datasets/mattop/chicago-cubs-batting-and-pitching-1876-2023)

This dataset offers a comprehensive archive of batting and pitching performances by the Chicago Cubs in Major League Baseball (MLB), covering every single year from the team's very beginning and creation all the way to the current year. This data set offers a robust number of statistics, including two CSV files that concentrate on batting and pitching statistics, respectively. 


## Research Questions
1. What impact does age have on baseball performance for players of the Chicago Cubs? We will use box plots, linear regressions, and t-tests to examine the relationship between age and runs, hits, doubles, triples, and home runs.
2. What hitting statistics (on base percentage, batting average, and slugging average), if any, have a relationship with the number of runs a player scores?
3. Does player position have an impact on batter performance? We will look at the player’s position in comparison to their runs, bases stolen, and home runs.
4. Does a pitcher’s overall performance impact game losses and wins? We will compare game losses and wins with pitcher variables such as hits per inning, runs allowed, and walks allowed.
5. Does a player’s dominant hand (i.e. left or right) have an impact on the player’s performance? We will do a comparison of hand dominance versus pitcher strikeouts.


## Communication Protocols
In order to update each other on the status of our individual parts of the project, we established frequent communication through Slack, class meetings, and the use of the asynchronous tools, Google Slides and Google Docs.

## Data Tools Used
- Cleaning Data: 
  - Python: Pandas
- Analyzing Data:
  - Python: Pandas, Matplotlib, Numpy, SciPy
- Report/README File:
  - Google Docs, VSCode
- Presentation:
  - Google Slides



## Analysis 
### Research Question 1
- Our null hypothesis for this research question is that age has no impact or no effect on player performance. In order to better understand if age had an impact on the performance of players of the Chicago Cubs, we first looked at linear regressions across five variables (per game): hits, runs, doubles, triples, and home runs. These variables were specifically chosen to account for potential scoring, which would seemingly be an indication of successful performance at bat. Additionally, when cleaning the data, if a player had less than 50 “at bats”, the data was dropped (to create the “filtered_players” data set). This cleaning was done to account for outliers of players who did not participate much at bat and accounted for situations such as pitchers who do not typically bat. 
- When measured against age, for the linear regressions, there is only a slight positive correlation for home runs per game. There is no correlation (a straight linear regression line) for doubles and hits per game. There is a slight negative correlation for triples and runs per game. Since the correlations were so slight for these linear regressions, the choice was made to create a box plot and then run an independent t-test specifically with home runs per game to see if any additional information could be gained. 
- To further investigate significance and create an additional visualization, a box plot was created for age against home runs per game, which did not show a linear relationship that increases the number of home runs.
- An independent t-test was run with two variables: ages equal to or more than 31 and ages under 31, against home runs per game. A slight statistical significance was found.
- Given this data and the visualizations, it can be said that there appears to be a slight positive correlation and a slight statistical significance with age as it impacts batting performance, specifically with home runs. This information would seem to indicate that age does have an impact on player performance at bat for the Chicago Cubs, which means we can reject the null hypothesis that age has no impact or effect on player performance. 


### Research Question 2
- Our second research question wanted to answer what hitting statistics (on base percentage, batting average, and slugging average) have a relationship with the number of runs a player scores? 
- Plotting runs scored against On Base Percentage showed there was a positive relationship. As a player’s on base percentage increases, so should the number of runs that the player scores. The more likely a player is to get on base, the more chances that a player will have an opportunity to score. We do see some outliers in this plot where we see a few players with high OBP and low runs scored. This may be due to some players that do not play in very many games and therefore will not have the same number of opportunities to score even though they have a higher OBP. 
- There is a positive relationship (slope) between AVG and runs scored. As a player's batting average increases, so should the number of runs that the player scores. As a player's batting average increases, the more likely they are to get a hit as a bat, and therefore be in a position to score.
- There is a positive relationship (slope) between SLG and runs scored. As an individual player's SLG increases, generally so should the number of runs that the player scores.


### Research Question 3
Which player position has the best performance as measured by runs, homeruns, and bases stolen?
- First, we created a bar graph which summarizes the count of Player Positions. This allowed us to group the dataset by Position, rather than rank and year, and to view how many players are in each position. The number of players in each position varies greatly.
- Next, we looked at the count of each performance measure for each position. Although the positions with the largest number of players don't always have the largest count, the positions that contain the fewest players consistently have the lowest count for each measure of performance.
- To control for the number of players in each position, we divided the count of each performance measure by the number of players in that position. This gives the average number of, for example, home runs per player in each position. We then used bar graphs to visualize the results. Referencing home runs again, the height of each bar represents the average number of home runs achieved by each position. Displaying the player position on the x-axis in descending order of popularity allows us to visually confirm that just because a position contains a larger number of players doesn't mean that particular position performs the best. 
- The results indicate that Right-fielders are most likely to perform the best in runs. Third- and first-basemen perform the second and third best, repectively. Right-fielders are also most likely to perform the best in homeruns. Left-fielders and first-basemen perform the second and third best, respectfully. Finally, second-basemen are most likely to perform the best in stealing bases. Outfielders and shortstops perform the second and third best, respectively.

### Research Question 4
Does a pitcher’s overall performance impact game losses and wins? 
- Adjusted ERA (ERA+) is ERA in relation to the entire league, as well as accounting for external factors like ballparks and opponents.
- The higher the ERA+ and the difference from the league average (100), the percent better or worse a particular pitcher is.
- The graph shows adjusted ERA in relation to win percentage, in which there is a rather consistent upward trend.


### Research Question 5
Does a player’s dominant hand (i.e. left or right) have an impact on the player’s performance? We will do a comparison of hand dominance versus pitcher strikeouts.
- The data distribution for the Chicago Cubs pitchers is 74.6% right handed VS 25.4% left handed.
- To answer this question we based the “Strikeouts Per Nine Innings” metric (K/9), determined by dividing the pitcher strikeout total by his innings pitched total and multiplying the result by nine.
- Through history both left and right pitchers performance has been fairly similar; a better performance in the early years for left handed pitchers, about the same performance starting in the 1920’s to early 2000’s. In recent years it has been more competitive and the data shows that lately there has been improvements on the left hand pitchers, resulting in a better performance in the "strikeout per nine innings" (K/9) metric.
- Overall we can see that the game has been increasingly more competitive over the years, having in average a better K/9 from both left and right hand pitchers. Having more strikeouts has created other issues with the game, being perceived as boring and consequently fandom has reduced. MLB has reacted to this and has implemented rules to improve the speed of the game to help bring more fans to the ballparks, larger bases and timed pitching/batting among other rules.


## Presentation
Our visualizations can be found on our [presentation slides](https://docs.google.com/presentation/d/1E0WVb5j7Sa7nxKiPKwricYTwQSbTrnU1LzUmB71TXM4/edit?usp=sharing).
