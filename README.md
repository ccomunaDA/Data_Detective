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

### Data Analysis (Step By Step Walkthough)

1. I opened SQL Lite Studio and downloaded the dataset 'sql-murder-mystery.db' to my computer. I then clicked on the "Add Database" button in SQL lite and selected the .db file.

2. Examine the tables contained within the dataset.

```
SELECT name 
FROM sqlite_master
WHERE type = 'table'
```
Result: 

![image](https://github.com/ccomunaDA/Data_Detective/assets/157404145/6539412b-306b-4b3a-9668-22e2576b4d31)

NOTE: Innitially I ran the code without the WHERE clause and some of the displayed results like "sqlite_autoindex_get_fit_now_member_1" struck me as odd. Upon looking the SQL Murder Mystery Website, I found that I was missing the 'table' designation. After running this with the WHERE clause as shown above, I was able to better understand the importance of designating the type of data you are requesting and the impact that that can have on results.

3. I opened the experienced prompt (Link in Files) and it read as follows:

"A crime has taken place and the detective needs your help. The detective gave you the crime scene report, but you somehow lost it. You vaguely remember that the crime was a ​murder​ that occurred sometime on ​Jan.15, 2018​ and that it took place in ​SQL City​. Start by retrieving the corresponding crime scene report from the police department’s database. If you want to get the most out of this mystery, try to work through it only using your SQL environment and refrain from using a notepad."

NOTE: Important information at a glance - /Date Jan.15, 2018/ - /SQL City/ - /Data in the crime scene report/ 

4. Pulled the crime scene report. 

```
SELECT *
FROM crime_scene_report
LIMIT 10
```
Result:

![image](https://github.com/ccomunaDA/Data_Detective/assets/157404145/77c0f45a-b399-4a4b-9fe7-a6d6d1aeefe3)

NOTES: Date is formatted as yearmonthday so since we are looking for Jan.15, 2018, it would look like 20180115. The type we are searching for is "murder" and the city we are looking for is "SQL City". Combining that with our previous code should look like:

```
SELECT *
FROM crime_scene_report
WHERE date = 20180115 AND type = "murder", and city = "SQL City"

```
Result:



NOTE: 

### Solution

### References
