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


* How does the weather impact average goals per match at home/away?

* How does attendance affect the scores?

* Has COVID-19 had an impact on home-team wins because of less attendance?



### Data collecting

We collect data for the most popular leagues - England, German, Spanish and Italian.

* Score data: 

    - https://www.football-data.co.uk/data
    
    
* Weather data: 

    - https://www.worldweatheronline.com/developer/
    
    - https://maps.googleapis.com/maps/api/place/findplacefromtext/output?parameters 


* Attendance data:

    - https://www.footballwebpages.co.uk


* Location data: cities and stadiums

    https://www.stadiumguide.com/premier-league-stadiums/
    https://www.bundesliga.com/en/bundesliga/news/stadiums-borussia-park-allianz-arena-signal-iduna-park-veltins-7642
    https://www.football-stadiums.co.uk/leagues/la-liga/ 
    https://www.worldfootball.net/venues/ita-serie-a-2019-2020/
    
    

### Data cleaning

* Identical items but different format

    - For the club names which vary in data source or language, we created unique id for each. 
    
    - For the date, we modified the date string to the form of year-month-date (month, date - two digits)
    

* Loading the data 

    - For not unified decoding, we used "ISO-8859-1"


* Attendance data

    - The attendance data for some matches are missing. We drop these rows.



### Analysis


* First, we combine the dataset.

    - The folder 'Resources' contains all raw data that we collected
    
    - The folder 'final-resources' contains the cleaned and combined data as csv files.


* To analyze the data, we code using jupyter notebook.

    - The folder 'final-code/datacleaning' contains the codes for producing combined and cleaned data.
    
    - The folder 'final-code/analysis' contains the codes for creating charts.   
    

* The charts are created to answer the the questions - Weather impact, Audience impact and Covid impact on games

    - The folder 'images' contains the output charts as png files.
    
    
### Observations


* go to Summary.md
