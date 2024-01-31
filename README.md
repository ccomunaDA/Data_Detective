# My First SQL Project 

This is where I will be documenting my process for how I solved The SQL Murder Mystery.

###### ![Dashboard](174092-clue-illustration.png)

### Table of Contents 


### Project Overview

"There's been a Murder in SQL City! The SQL Murder Mystery is designed to be both a self-directed lesson to learn SQL concepts and commands and a fun game for experienced SQL users to solve an intriguing crime."

This project can be tackled in two ways: 
1. For a more beginner friendly approach, the [SQL Murder Mystery Website](https://mystery.knightlab.com) contains SQL Lite Editors built in with some helpful instructions. 
2. For a more experienced approach and the one I will be following, I chose to work from the experienced prompt which can be [Viewed Here](prompt_experienced.pdf).

### Data Sources

Data File: The primary dataset used for this analysis is the "sql-murder-mystery.db" file, containing the relevant tables that would be used to crack this case. 

### Tools

- SQL Lite Studio [Download Here](https://sqlitestudio.pl)
- SQL Murder Mystery Website to follow along [Click Here](https://mystery.knightlab.com/#experienced)
- 
### Data Analysis (Step By Step Walkthough)
1. Examine the tables contained within the dataset.
   
```
SELECT name 
FROM sqlite_master
WHERE type = 'table'
```
Note: Innitially I ran the code without the WHERE clause and some of the displayed results like "sqlite_autoindex_get_fit_now_member_1" struck me as odd. Upon looking the SQL Murder Mystery Website, I found that I was missing the 'table' designation. After running this with the WHERE clause as shown above, I was able to better understand the importance of designating the type of data you are requesting and the impact that that can have on results.

2. I opened the experienced prompt (Link in Files) 

### Solution

### References
