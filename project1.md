# College Football Recruiting and Team Success

## Research Question

**What is the relationship between a college football team's recruiting strength and its on-field success among FBS teams?**

A related question for this project is:

**Do teams with higher-rated recruiting classes tend to have higher winning percentages and stronger overall team ratings?**

---

## 1. Problem Definition

College football recruiting is often used as a way to predict the future success of a program. Teams that consistently recruit highly rated players are generally expected to perform better on the field. However, strong recruiting does not automatically guarantee that a team will win games.

The purpose of this project is to examine the relationship between recruiting strength and on-field performance among FBS college football teams.

The main research question is:

**What is the relationship between a college football team's recruiting strength and its on-field success among FBS teams?**

A related question is whether teams with higher-rated recruiting classes tend to have higher winning percentages and stronger overall team ratings.

To measure team success, I plan to examine variables such as winning percentage, point differential, and potentially a team rating such as Elo or SP+.

This question is relevant because recruiting rankings are widely used by college football fans, coaches, analysts, and media organizations when discussing the future strength of programs. Comparing recruiting results with actual team performance can help show how strongly recruiting strength is associated with success on the field.

---

## 2. Data Description

The data for this project comes from the **College Football Data API (CFBD)**.

College Football Data provides historical information about college football, including recruiting data, game results, team information, rankings, and advanced team statistics.

Source: [College Football Data](https://collegefootballdata.com)

I plan to collect recruiting and team performance data for multiple FBS seasons and combine the datasets for analysis.

Each observation in the final dataset will represent one **team during one season**, also called a team-season observation.

The main variables used in the analysis are:

- Team
- Season
- Recruiting strength
- Recruiting ranking or recruiting score
- Wins
- Losses
- Winning percentage
- Points scored
- Points allowed
- Point differential
- Potential team performance rating such as Elo or SP+

The final dataset contains:

- **Rows:** [ADD AFTER RUNNING NOTEBOOK]
- **Columns:** [ADD AFTER RUNNING NOTEBOOK]

Missing values:

**[ADD AFTER RUNNING NOTEBOOK]**

The data was collected through an API rather than manually entering information or using a pre-built spreadsheet.

---

## 3. Variables and Important Context

### Recruiting Strength

**Conceptual definition:**  
Recruiting strength represents the overall quality of players recruited by a college football program.

**Operational definition:**  
Recruiting strength will be measured using a team's recruiting ranking or recruiting score provided through the College Football Data API.

---

### Winning Percentage

**Conceptual definition:**  
Winning percentage represents the proportion of games a team wins during a season.

**Operational definition:**  
Winning percentage will be calculated by dividing a team's number of wins by its total number of games played.

`Winning Percentage = Wins / Games Played`

---

### Wins and Losses

**Conceptual definition:**  
Wins and losses represent the number of games a college football team won or lost during a season.

**Operational definition:**  
Wins and losses will be obtained from team season performance data collected through the College Football Data API.

---

### Point Differential

**Conceptual definition:**  
Point differential represents the difference between the total number of points a team scores and the total number of points scored by its opponents.

**Operational definition:**  
Point differential will be calculated as:

`Point Differential = Points Scored - Points Allowed`

A positive point differential means that a team scored more points than it allowed during the season. A negative point differential means that the team allowed more points than it scored.

---

### Team Rating

**Conceptual definition:**  
A team rating is a numerical estimate of the overall strength of a college football team.

**Operational definition:**  
If an appropriate measure is available through the College Football Data API, a team rating such as Elo or SP+ may be used as an additional measure of on-field performance.

---

### Season

**Conceptual definition:**  
Season represents the college football season in which the team's performance occurred.

**Operational definition:**  
Season will be represented using the season year provided by the College Football Data API.

---

### Team

**Conceptual definition:**  
Team represents an individual NCAA FBS college football program.

**Operational definition:**  
Teams will be identified using the program names provided by the College Football Data API.

---

## 4. Data Cleaning and Preparation

The recruiting data and team performance data come from different parts of the College Football Data API, so the datasets need to be cleaned and combined before analysis.

I will use Python and pandas to inspect, clean, and prepare the data.

The main cleaning and preparation steps include:

1. Importing the recruiting and team performance data from the College Football Data API.
2. Inspecting the datasets to understand their rows, columns, and data types.
3. Selecting the variables that are relevant to the research question.
4. Restricting the analysis to FBS college football teams.
5. Checking for missing values.
6. Checking for duplicate observations.
7. Making sure team names and season values match between datasets.
8. Combining recruiting data and team performance data using team and season.
9. Calculating winning percentage.
10. Calculating point differential if points scored and points allowed are available.
11. Removing or addressing observations that are missing information required for the analysis.

Observations that are missing recruiting information or performance information may need to be removed because both types of information are necessary to answer the research question.

The exact number of observations removed and the amount of missing data will be reported after the data cleaning process is completed.

---

## 5. Visualizations and Insights

### Visualization 1: Recruiting Strength and Winning Percentage

The first visualization will be a scatter plot comparing recruiting strength with season winning percentage.

Each point will represent one FBS team during one season.

**X-axis:** Recruiting strength  
**Y-axis:** Winning percentage

This visualization will help show whether teams with stronger recruiting classes tend to win a greater percentage of their games.

**Result:**

[ADD DESCRIPTION AFTER CREATING GRAPH]

---

### Visualization 2: Recruiting Strength and Team Performance

The second visualization will compare recruiting strength with another measure of team performance.

Possible measures include:

- Point differential
- Elo rating
- SP+ rating

A trend line may also be included to make the overall relationship easier to see.

**X-axis:** Recruiting strength  
**Y-axis:** Team performance measure

**Result:**

[ADD DESCRIPTION AFTER CREATING GRAPH]

---

## 6. Storytelling and Conclusions

The purpose of this analysis is to determine whether stronger recruiting is associated with greater on-field success in FBS college football.

If teams with stronger recruiting classes tend to have higher winning percentages, stronger point differentials, or higher team ratings, this would suggest that recruiting strength and team success are related.

However, this analysis cannot prove that recruiting strength directly causes teams to win more games.

College football performance is affected by many other factors, including coaching, player development, injuries, transfers, strength of schedule, conference strength, and game-to-game variation.

The visualizations and statistical results will be used to determine how strong the relationship appears to be in the data.

### Final Conclusion

[ADD FINAL CONCLUSION AFTER ANALYSIS]

---

## 7. Limitations, Ethics, and Reflection

There are several limitations to this analysis.

First, recruiting rankings are estimates of player talent and are not perfect measurements. Players may improve or decline after entering college, and recruiting services may evaluate players differently.

Second, college football teams do not play identical schedules. Some teams face significantly stronger opponents than others. Because of this, winning percentage and point differential may not represent the same level of performance for every program.

The analysis also does not fully account for factors such as:

- Coaching quality
- Player development
- Injuries
- Transfer portal additions
- Transfer portal losses
- Strength of schedule
- Conference strength
- Coaching changes
- Player playing time
- Players leaving early for professional football

Another limitation involves the timing of recruiting classes. Players usually remain with a college football program for multiple seasons. This means that a team's performance during one season may be influenced by several previous recruiting classes rather than only one recruiting class.

From an ethical perspective, recruiting ratings should also be interpreted carefully. A recruiting rating is an estimate of a player's ability at one point in time and should not be treated as a complete measure of that player's ability, value, or future performance.

The results of this project should therefore be interpreted as a relationship between recruiting measures and team performance rather than proof that recruiting rankings determine team success.

If I had more time and additional data, I would like to examine several previous recruiting classes together and account for strength of schedule, transfer portal activity, and coaching changes.

---

## 8. References

### Data Source

College Football Data. (n.d.). *College Football Data*.  
https://collegefootballdata.com

### Peer-Reviewed Academic Sources

**Source 1:**  
[ADD PEER-REVIEWED SOURCE]

**Source 2:**  
[ADD PEER-REVIEWED SOURCE]

**Source 3:**  
[ADD PEER-REVIEWED SOURCE]

---

## 9. Code and AI Transparency

The complete Python code used to collect, clean, analyze, and visualize the data for this project is available through the project's GitHub repository.

[View the Jupyter Notebook](project1.ipynb)

### AI Usage Disclosure

I used OpenAI ChatGPT (GPT-5.6) during this project to help interpret the assignment requirements, organize the structure of the analysis, troubleshoot Python code, and improve explanations of analytical decisions. I reviewed the suggestions and am responsible for the final code, analysis, visualizations, and written content included in this project.
