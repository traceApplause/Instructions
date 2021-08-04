# Instructions

Pull both projects. Gradle is used for the spring boot project if relevant. change application.properties in java project for datasource config if neccessary.

For data input on client, enter data into text boxes as comma delimited with no spaces
example: US,GB not US, GB
spaces are valid inside of device name ie: 
iPhone 4,Nexus 4 is valid
iPhone 4, Nexus 4 is not 


for database construction:
create database named 'applause_exercise'
copy content of Instructions/SQL Creation into SQL Commander tab, execute for creation of tables

place csv files into 'C:/pathTo/MySQL Server 8.0/Uploads/place_here.csv'

run query:

LOAD DATA INFILE 'C:/pathTo/MySQL Server 8.0/Uploads/testers.csv'
INTO TABLE tester
FIELDS TERMINATED BY ','
ENCLOSED BY '"'
ESCAPED BY '\\'
LINES TERMINATED BY '\n'
IGNORE 1 ROWS;

in SQL Commander tab, replacing file name and table name for all 4 csv files(devices, bugs, testers, tester_device)
should populate data into all 4 tables
