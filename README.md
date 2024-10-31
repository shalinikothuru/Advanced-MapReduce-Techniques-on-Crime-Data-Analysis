Installation Requirements:
Java
Hadoop
IntelliJ IDEA

TASK 2: 
-------
Use the following commands to create bda_assignment_5 directory in hdfs and copy csv files from local to hadoop.

hdfs dfs -mkdir /bda_assignment_5
hdfs dfs -mkdir /bda_assignment_5/task2

hdfs dfs -copyFromLocal "D:\MSCS Course\1.3\BDA\Assignments\Assignment 5\Violence_Reduction_-_Victims_of_Homicides_and_Non-Fatal_Shootings-1.csv" /bda_assignment_5
hdfs dfs -copyFromLocal "D:\MSCS Course\1.3\BDA\Assignments\Assignment 5\Violence_Reduction_-_Victim_Demographics_-_Aggregated.csv" /bda_assignment_5

hdfs dfs -mv /bda_assignment_5/Violence_Reduction_-_Victim_Demographics_-_Aggregated.csv /bda_assignment_5/dataset1.csv
hdfs dfs -mv /bda_assignment_5/Violence_Reduction_-_Victims_of_Homicides_and_Non-Fatal_Shootings-1.csv /bda_assignment_5/dataset2.csv

Once you have the datasets in hadoop, open IntelliJ IDEA and run the program. Before that, you have to maven clean and install to compile the source code and package it into a jar file.

My jar file name : bda_5-1.0-SNAPSHOT.jar

To execute the program, please run the following command in terminal
cmd: hadoop jar target/bda_5-1.0-SNAPSHOT.jar bda_5.JoinRunner /bda_assignment_5/dataset1.csv /bda_assignment_5/dataset2.csv /bda_assignment_5/task2/results

Once the program exceution completes, you can view the results in hadoop and you can download the file.

TASK 3:
-------
Use the following commands to create task3 directory.

hdfs dfs -mkdir /bda_assignment_5/task3

To execute the program - task 3, please run the following command in terminal
cmd: hadoop jar target/bda_5-1.0-SNAPSHOT.jar bda_5.JoinRunner /bda_assignment_5/dataset1.csv /bda_assignment_5/dataset2.csv /bda_assignment_5/task3/results

Once the program exceution completes, you can view the results in hadoop and you can download the file.