# project-one

## Soccer - Is home team advantage real? 


### Members: 

* Alyssa George 
* Niral Patel 
* Andrew Giermak
* Eunjeong Lee 


### Project Description/Outline:

The scope of this project is to review international soccer data in the European leagues to solve the question of whether or not home team advantage is real. This will cover a few common assumptions such as home team advantage is real because there are more fans in the stadium or home team advantage is real because they are more used to the weather. We will be able to potentially predict how the rest of the season will continue without fans in the stadiums.
Key things we will analyze may include but are not limited to the following: 



### Data collecting

* Stadiums & City

    https://www.stadiumguide.com/premier-league-stadiums/
    https://www.bundesliga.com/en/bundesliga/news/stadiums-borussia-park-allianz-arena-signal-iduna-park-veltins-7642
    https://www.football-stadiums.co.uk/leagues/la-liga/   --- and wikipedia
    https://www.worldfootball.net/venues/ita-serie-a-2019-2020/


* Attendances : for each league, team

    https://www.footballwebpages.co.uk/fc-augsburg/attendances
    
    

### Data cleaning

* Names : different names

* column "Unnamed 11".. delete

* Date : 
    different formats : ex) 06/07/2019  vs. 6/7/2019
    to_datetime misconducting result: ex) 1/12/19 ---> 2019-01-12, but this is 2019-12-01

* Decoding --- not unified decoding -- used "ISO-8859-1"

* Before Covid, there are matches of which attendance are not available. : drop

  SER half number of matches are filtered out.
...............



### Analysis


#### How does the weather impact average points per match at home/away?

* For each league, we create a dataframe of columns

  - (Home)Team, Match Date, City, Weather(Temp. Heat. Humidity), Score, Score of Op, Results(Win/Lose)
  
  - (Away)Team, Match Date, City, Weather(Temp. Heat. Humidity), Score, Score of Op, Results(Win/Lose)

* Plots of Weather vs. Score (Use legend or subplots)

Scatter plot and linear regression: Choose one day.

  1.  Home
  
  - Weather values on that day for all stadiums (xvalue)
  - Home scores of all matches
  ???- Average of total scores of match for same weather fact (?)
  
  
  2. Away
  
  - Weather values on that day for all stadiums (xvalue)
  - Away scores of all matches
  ???- Average of total scores of match for same weather fact
  
  
* Plots of Weather vs. Wins (Use legend or subplots) : Scatter plot and linear regression

  1.  Home
  - Weather value (xvalue)
  - Average of wins for same weather fact
  
  2. Away
  - Weather value (xvalue)
  - Average of wins for same weather fact

##### How does attendance affect score?

* For each league, we create a dataframe of columns

  - (Home)Team, Avg Score, Avg. Results(Win/Lose), Avg. Attendance, Avg. Occupancy
  
  - (Away)Team, Avg Score, Avg. Results(Win/Lose), Avg. Attendance

* Plots of Attendance vs. Score (Use legend or subplots) : Scatter plot and linear regression

  1.  Home
  - Attendances value (xvalue)  
  - Average of total scores of match for same attendances

  2. Away
  - Attendances value (xvalue)
  - Average of total scores of match for same attendances
  
* Plots of Attendances vs. Score for selected teams : Scatter plots with size of dots

  (We choose top teams??)
  
  1.  Home
  - xvalue = Game dates (xvalue)  
  - yvalue = Avg. Scores of the month
  - size = Attendances

  2. Away
  - xvalue = Game dates (xvalue)  
  - yvalue = Avg. Scores of the month
  - size = Attendances

#### Has COVID-19 had an impact on home-team wins because of less attendance?

* For each league, we create a dataframe of columns, before Covid-19 and after,

  - (Home)Team, Avg Score(Before), Avg. Score(After), Avg. Occupancy
  
  - (Away)Team, Avg Score(Before), Avg. Score(After), Avg. Occupancy

* Plots of Scores(Before and After) of teams : Stacked bar graphs

  1.  Home
  - Before Avg. Score (yvalue) 
  - After Avg. Score (yvalue)  
  - Teams (xticks)
  
  2. Away
  - Before Avg. Score (yvalue) 
  - After Avg. Score (yvalue)  
  - Teams (xticks)


### Observations and Insights - Story/Truth telling

* What is the probability that you will win/lose/draw for home vs away?
