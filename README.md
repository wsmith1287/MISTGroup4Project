# MISTGroup4Project
Team Members & GitHub Repository Links:

Ryan Dean: @RDean45

Ryan Kelly: @Rjk4133

Cameron Smith: @camjshmitt

Wyatt Smith: @wsmith1287 

Mattie Garett: @MatGar22

Lilly Wood: @lillywood21


# Problem Description:
The problem that we are trying to solve has to do with the creation of a working database that consolidates data for a soccer club into a functioning model. The main entity that comprises this data and the model is the Team entity which is made up of the different teams that comprise the soccer club and includes information such as their team name and where their home field is. In addition to this, we have other entities such as data on the players that comprise these teams, the statistics for each of these players, the coaching staff that make up the soccer club, and much more. In addition to a working model, we hope to build many working queries that provide data to possible stakeholders of the soccer club to make well informed complex decisions regarding the clubs activities. With this complex data model and the many different queries we hope to deliver working data that can be used by the soccer club to operate at an increased efficiency level and deliver better value to its stakeholders.



# Data Model:
Data Model Description:


Our model is structured like a football (soccer) academy. The Teams entity represents the information stored about each of the different teams in the club including the team ID, the team name, the team’s home field and more. Teams have many matches, which is shown by the one to many identifying relationship between Teams and Teams Have Matches. Teams also have head coaches which is represented by the one to one non identifying relationship between Teams and the entity Coaching Staff. Teams have many coaches which is shown by the one to many non identifying relationship between Teams and Coaching Staff. Teams may also have many sponsors which is represented by the one to many identifying relationship between Teams and the Teams Have Sponsors entity. Teams have many players which is shown by the one to many non identifying relationship between Teams and Player Information. Teams also have captains which are represented by the one to one non identifying relationship between Teams and Player Information.

Player Information stores data like the player’s player ID, the player’s first and last name, their age and much more. Player Information has many Player Stats which is shown by the one to many identifying relationship between Player Information and Player Stats. Player Information also has many Injury Reports which is represented by the one to many identifying relationship between Player Information and Injury Report. 

Teams Have Matches stores information on the match date, venue and more. Teams Have Matches stores many player stats which is shown by the one to many identifying relationship between Player Stats and Teams Have Matches. 

Match stores data on the match ID, match type and more. Match is made up of many different individual matches which is represented by the one to many identifying relationship between Match and Teams Have Matches. 

Divisions store information on the division ID, the division name, the division age group, the division skill level and more. Divisions have many matches which is shown by the one to many non identifying relationship between Divisions and Match. Divisions are made up of many different teams which is represented by the one to many non identifying relationship between Divisions and Teams. 




# Data Dictionary:


# Ten Queries:


# Database Information:
