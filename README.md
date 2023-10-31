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


Player Information stores data like the player’s player ID, the player’s first and last name, their age and much more. Players have many statistical instances recorded which is represented by the one to many relationship between Player Information and Player Stats. Player Stats stores information pertaining to the saves, goals scored, minutes played, and penalties of each player during each match for a specific team. Players can also have many Injury Reports which is represented by the one to many identifying relationship between Player Information and Injury Report. Injury report has information regarding the injury such as the reportID, type of injury that occurred, and estimated recovery timeline. 


Teams Have Matches stores information on the match date, venue and more. Teams Have Matches stores many player stats which is shown by the one to many identifying relationship between Player Stats and Teams Have Matches. 


Matches stores data on the match ID, match type and more. Matches is made up of many different individual matches which is represented by the one to many identifying relationship between Match and Teams Have Matches. 


Divisions store information on the division ID, the division name, the division age group, the division skill level and more. Divisions have many matches which is shown by the one to many non identifying relationship between Divisions and Match. Divisions are made up of many different teams which is represented by the one to many non identifying relationship between Divisions and Teams. 


The league entity stores data on the league ID, the league name, the league president, the date founded, and much more. A league is many up of many Divisions which is represented by the one to many non identifying relationship between League and Divisions. 


The Sponsor entity stores information including the sponsor ID, the sponsor name, and the phone number associated with the sponsor. A sponsor makes up a list of many different sponsors which is represented by the one to many identifying relationship between Sponsor and Teams Have Sponsors. The Teams Have Sponsors table is an associative entity created by the many to many relationship between Teams and Sponsors. The Teams Have Sponsors entity stores data such as the date of sponsorship and amount of sponsorship.


Coaching Staff stores data including the coach ID, the coach’s first and last name, the number of years they have coached, their date of birth, their date of birth, and much more. Coaching Staff at the football club report to Head Coaches which is shown by the one to many non identifying recursive relationship between Coaching Staff. Coaching Staff hold many training sessions which is represented by the one to many non identifying relationship between Coaching Staff and Training Sessions. 


Training Sessions store information on the session ID, the practice date, and more. Training Sessions can require many field reservations depending on the type of drills run which is represented by the one to many identifying relationship between Training Sessions and Field Reservation. Field reservations stores data including a composite primary key of fieldID and sessionID along with data such as reservation status and the date and time reserved.

<img width="870" alt="Screenshot 2023-10-31 at 3 07 54 PM" src="https://github.com/wsmith1287/MISTGroup4Project/assets/148778195/5772ccfe-e6c9-42a1-94f5-ae758b264257">




# Data Dictionary:
https://docs.google.com/spreadsheets/d/13dZfk5lfz4i-kXLNsyzoN23wI5GA-gJi/edit#gid=347490538

# Ten Queries:
Query 1 allows the academy to see what teams score the most goals and their percentage share of total goals scored within the league. This information could be useful, as teams that score a higher percentage of goals in the league would be more likely to get moved to a higher skill division. Teams should be competitive in their division, but not overly competitive as this could result in a skill level imbalance. 

Query 2 shows the captains of each team and a ranking of captains by number of goals scored in their career at the Georgia United Soccer Academy. This information is useful in determining the most accomplished team captains for end of season awards and can help to determine future college soccer options.

Query 3 allows the Georgia United Soccer Academy to see what coaches are canceling their field reservations and at what rate. This allows management to better manage field reservations, as coaches that tend to cancel their reservations most often get last pick after other coaches select their fields for practice.

Query 4 shows the league how much money teams have received from their sponsors. This information can be used to spearhead fundraising and new sponsorship outreach efforts for teams with smaller cash inflows from sponsors. This can help teams keep down costs of travel and uniforms for its players.

Query 5 helps the Georgia United Soccer Academy identify conditioning coaches that may be up for promotion soon. The academy is always looking for Coaching Staff members that show loyalty and have coached for more than 10 years for promotions.

Query 6 shows the soccer academy which players are available to join a team that are not already on one. This would allow coaches to search for players available to play certain positions where they may need another player and also lets the league know which children need to be placed with a team still. 

Query 7 helps coaches and teams figure out which players are more likely to have penalties than others, which can be an important stat for teams to track about their own players, and their opponents. From a behavioral standpoint as this is a youth league, it is important to identify who is committing far more penalties than their peers in order to intervene while they are still developing. This data can be used by coaches to organize meetings with their players in order to correct this behavior.

Query 8 shows which players in the Football club have had an ACL injury before. This is important information for the club to keep track of a major injury like this that keeps players out for up to 9 months. If they have a lot of non contact injuries, they might want to consider moving from turf to grass or other preventative measures. In addition to this, the data will show which players are most prone to injury and coaches can take precautions to protect their players. 

Query 9 highlights potential organizational mismanagement within teams and shows the assistant coaches who have more experience than the current head coach they report to. If the season does not go well, this list would provide the basis for potential organizational restructuring and list the coaches who could become the new head coach on their current team.

Query 10 lists the total goals scored by a team that won or tied their match in matches that are classified as competitive. This is useful information as it provides a clear record of which team won each individual match in the matches that are competitive and can be used potentially as the basis of an exterior league standings table that assigns points based on wins and losses.
<img width="862" alt="Screenshot 2023-10-31 at 3 06 03 PM" src="https://github.com/wsmith1287/MISTGroup4Project/assets/148778195/1100f52f-77ac-4de5-94c9-2b1923c6f606">


# Database Information:
Database Name: ns_F2329704Group4
