# ICC Cricket World Cup 2023 Analysis

## 📌 Project Overview

This project provides a comprehensive data analysis of the **ICC Cricket World Cup 2023** using Python.

The analysis covers multiple aspects of the tournament, including:

- Team performance
- Batting strength and depth
- Bowling performance
- Venue performance
- Batting and bowling statistics
- Top-performing batsmen
- Top-performing bowlers
- Match outcomes
- Batting first vs chasing performance

The objective is to use data analysis and visualization to identify important patterns and insights from the tournament.

---

## 🎯 Objectives

The main objectives of this project are:

- Analyze team win percentages.
- Evaluate batting strength and batting depth.
- Analyze average runs scored per wicket.
- Compare batting performances across teams.
- Analyze bowling performances.
- Study the effect of batting first versus chasing.
- Analyze average first-innings scores by venue.
- Identify the top batsmen based on different performance metrics.
- Identify the top bowlers based on different bowling metrics.
- Visualize important tournament statistics.

---

## 🗂️ Datasets

The analysis uses four datasets:

### 1. `batting_summary.csv`

Contains batting performance for players across World Cup matches.

Important columns include:

- `match_no`
- `batsman_name`
- `team_innings`
- `runs`
- `balls`
- `4s`
- `6s`
- `strike_rate`
- `dismissal`
- `batting_position`

### 2. `bowling_summary.csv`

Contains bowling performance for players across matches.

Important columns include:

- `match_no`
- `bowler_name`
- `bowling_team`
- `overs`
- `maidens`
- `runs`
- `wickets`
- `economy`

### 3. `match_schedule_results.csv`

Contains match-level information.

Important columns include:

- Match number
- Date
- Venue
- Team 1
- Team 2
- Winner

### 4. `world_cup_players_info.csv`

Contains player information, including:

- Player name
- Team
- Playing role

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## 🔄 Data Preprocessing

Before performing the analysis, the datasets were cleaned and standardized.

### Column Name Standardization

Column names were:

- Stripped of extra spaces
- Converted to lowercase
- Converted to snake_case
- Cleaned of special characters

### Column Renaming

Columns were renamed across datasets to maintain consistent naming.

For example:

- `match_no` → `match_id`
- `batsman_name` → `batsman`
- `team_innings` → `team`
- `bowler_name` → `bowler`
- `bowling_team` → `team`

### Text Cleaning

Extra spaces were removed from:

- Team names
- Player names
- Match winners

Dismissal information was also standardized into:

- `out`
- `not out`

### Data Integration

The batting and bowling datasets were merged with the player information dataset using player names.

This allowed player-level analysis to include:

- Country/team
- Playing role

### Numeric Conversion

Batting and bowling statistics were converted into appropriate numeric data types.

For example:

- Runs
- Balls
- Fours
- Sixes
- Strike rate
- Overs
- Maidens
- Wickets
- Economy

### Date Processing

Match dates were converted into datetime format.

An innings column was also created for batting data based on the batting order of the two teams in each match.

---

# 📊 Analysis Performed

## 1. Team Analysis

The first part of the analysis focuses on team performance.

For each team, the analysis calculates:

- Total matches played
- Total wins
- Win percentage

The results are visualized using a bar chart showing the win percentage of each team during the ICC Cricket World Cup 2023.

---

## 2. Batting Strength and Depth

The batting position of each player is categorized into three groups:

### Top Order
Positions 1–3

### Middle Order
Positions 4–7

### Lower Order
Positions 8+

The analysis then calculates team-level innings statistics, including:

- Total runs
- Wickets lost
- Runs per wicket

Average runs per wicket are calculated for each team to provide an indication of batting performance and depth.

---

## 3. Venue Analysis

The project analyzes how teams performed depending on whether they:

- Batted first
- Chased a target

Win percentages are calculated for both situations at different venues.

This is visualized using a grouped bar chart comparing:

- Batting First Win %
- Chasing Win %

The analysis also calculates the average first-innings score for each venue.

---

## 4. Top Batsmen Analysis

Detailed batting statistics are calculated for each batsman.

The metrics include:

- Total runs
- Matches played
- Innings played
- Times dismissed
- Times not out
- Highest score
- Total balls faced
- Total fours
- Total sixes
- Batting average
- Strike rate
- Number of centuries
- Number of half-centuries

### Top 10 Run Scorers

The top 10 batsmen are identified based on total runs scored.

### Highest Batting Average

The top batsmen by batting average are identified after applying a minimum threshold of **200 total runs**.

### Highest Strike Rate

The top batsmen by strike rate are identified using the same minimum threshold of **200 runs**.

### Most 50+ Scores

The analysis also identifies players with the highest number of combined:

- Centuries
- Half-centuries

---

## 5. Top Bowlers Analysis

Detailed bowling statistics are calculated for each bowler.

The metrics include:

- Total wickets
- Runs conceded
- Total overs
- Maidens
- Matches played
- Bowling innings
- Bowling average
- Economy rate
- Bowling strike rate
- Best bowling figures

### Top 10 Wicket Takers

The top 10 bowlers are identified based on total wickets.

### Best Bowling Average

The analysis identifies bowlers with the lowest bowling average, using a minimum threshold of **10 wickets**.

### Best Economy Rate

The bowlers with the lowest economy rates are identified.

### Best Bowling Strike Rate

The analysis identifies bowlers with the lowest strike rate, using a minimum threshold of **10 wickets**.

For bowling strike rate, a lower value represents fewer balls required per wicket.

---

# 📈 Visualizations

The project contains multiple visualizations, including:

- Team win percentage
- Average runs per wicket by team
- Batting performance comparisons
- Venue-based win percentages
- Batting first vs chasing performance
- Average first-innings score by venue
- Top 10 batsmen by total runs
- Top batsmen by batting average
- Top batsmen by strike rate
- Most 50+ scores
- Top 10 bowlers by wickets
- Best bowling averages
- Best economy rates
- Best bowling strike rates

---

# 💡 Key Insights

The analysis provides insights into different dimensions of the ICC Cricket World Cup 2023.

### Team Performance

Team win percentages provide a comparison of how frequently teams converted their matches into victories during the tournament.

### Batting

The runs-per-wicket analysis provides an indication of how effectively teams converted wickets into runs.

Breaking batting positions into top-order, middle-order, and lower-order groups also provides a way to examine batting depth.

### Venue Performance

The venue analysis compares the outcomes of teams batting first and teams chasing.

It also shows how average first-innings scores varied across venues.

### Batsmen

The project evaluates batsmen using multiple metrics rather than relying only on total runs.

These include:

- Batting average
- Strike rate
- Total runs
- Centuries
- Half-centuries

### Bowlers

Similarly, bowlers are evaluated using several metrics:

- Total wickets
- Bowling average
- Economy rate
- Strike rate
- Best bowling figures

This provides a broader view of bowling performance during the tournament.

---

# 📁 Project Structure

```text
ICC-Cricket-World-Cup-2023-Analysis/
│
├── ICC Cricket World Cup 2023 Analysis Report.ipynb
│
├── batting_summary.csv
├── bowling_summary.csv
├── match_schedule_results.csv
├── world_cup_players_info.csv
│
└── README.md
