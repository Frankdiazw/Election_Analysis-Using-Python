# Election Analysis using Python :bar_chart::snake:

![](https://github.com/Frankdiazw/Election_Analysis/blob/main/Resources/Elections-Image.png)

## Overview of Project:mag_right:
This document focuses on reporting the election results for an election audit of the tabulated results for U.S. congressional precinct in Colorado. Using python to import the tabulated results to the IDE and showcase the election results to a text file. In this document, a series of votes were processed and filtered to obtain the total number of votes, the number of votes each candidate obtained and their percentage, and the majority winner of the Colorado elections. Excel is commonly used for this type of data, but in this case an automation of it was sought in Python in order to be able to use this code for other and future elections.

## Election Audit Results:woman::man::man::statue_of_liberty:
The election results where the following:

![](https://github.com/Frankdiazw/Election_Analysis/blob/main/Resources/Electionresults.png)

- **Figure 1. Election Results shown in the Terminal of Visual Studio Code.**

In base of the Figure above and the program made for this elections, five analysis and methods can be described from the electoral precint:
- A variable was created to store the number of votes in it (integer data type), a for loop was created in the Excel row to count the number of votes in the elections, resulting in: 369, 711 votes.
  - The function: total_votes + = 1 was used to count the number of votes that there were during the elections.
  
- Based on the total number of votes (369,711), each county obtained a certain percentage of number votes based on the total number of votes received in Colorado. It can be interpreted as follows using the basic formula for calculating percentages adapted to Python: vote_percentage = float (votes) / float (total_votes2) * 100, each variable was previously declared.
  - Jefferson summed 38,855 votes out of 369,711 total votes, resulting in 10.5% in the electoral precinct.
  - Denver summed 306,055 votes out of 369,711 total votes, resulting in 82.8% in the electoral precinct.
  - Arapahoe summed 24,801 votes out of 369,711 total votes, resulting in 6.7% in the electoral precinct.
  
- In order to determine which of the counties had the most votes, an if statement was used to determine which county summed more votes, using the following code: if (votes_county > winning_count) and (vote_percentage_county > winning_percentage), all variables where previously declared and the result was saved in the variable: winning_county. 
  - In base of this statement, Denver resulted the county with the majority of votes, with 306,055, representing the 82.8% of the 100% of the votes.
 
- Now, talking about the candidates, a similar code was structured using an if statement inside a for loop to retrieve the number of votes each candidate recieved from each county and an if statement to determine which candidate won the elections, the outcomes are shown below:
  - To retrieve the number of votes each candidate recieved, a variable was created to save the loop through the candidate's row, then an if statement was declared to add the number of votes of each candidate's name, resulting in the end: candidate_votes[candidate_name] += 1.
  - To determine which candidate recieved the most votes, first a for statement looped over the three contestants repeating an if statement on each contestant to determine who got more votes, then printing the result on the text file. 
  
- Based on the candidates analysis made above, the candidate results were the following:
  - Charles Casper Stockham obtained 85,213 votes out of 369,711 total votes, resulting in 23.0% in the electoral precinct.
  - Diana DeGette obtained 272,892 votes out of 369,711 total votes, resulting in 73.8% in the electoral precinct.
  - Raymon Anthony Doane obtained 11,606 votes out of 369,711 total votes, resulting in 3.1% in the electoral precinct.
 
:white_check_mark: The Winner of the U.S. congressional precinct in Colorado was: **Diana DeGette** with the **73.8% (272,892)** of the total votes.

### Description of code used to run the Election Analysis :computer:
Click in the following link to see a detailed description of the code used in the workbook:
- :page_with_curl: [Python code for Election Analysis](https://github.com/Frankdiazw/Election_Analysis/blob/main/PyPoll_Challenge_starter_code.py)

## Election Audit Summary:scissors::pencil2:
The mentioned script is used in the U.S. congressional precinct in Colorado elections to automate the electoral process, in order to obtain a much faster and more accurate response. This script can not only be used for these precinct elections, but for any type of elections, be it State or Federal, this program is capable of performing the same tasks.
Regarding the above, minuscule changes should be made to the Script in order to avoid syntax errors, the changes are as follows:
1. The path of the extraction file must be changed, the new data table must be declared with the following syntax:
  - file_to_load = os.path.join ("Folder", "name_of_archive.csv").
2. Although the same variables could be left, this step is not so necessary, even as a good programmer, some variables should be renamed since it would not make sense to find a variable named for counties in data that are for states in a presidential election. 
  - Example: largest_county = "", it could be changed to largest_state = "".
3. To get the name of any candidate or state, etc. The function was used:
county_name = row [1], where row [1] is used to loop in the row where you want to get the names. The programmer must identify in which row the information he wants to obtain from the new spreadsheet is located, he must use the following syntax so that errors do not occur when running the program: variable_name = row [x], where x means the row number where the required information is found (remember that it starts counting from 0).
