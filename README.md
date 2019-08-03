# CreditCardManagement_Hadoop_Sqoop

Credit-card-management-system-Hadoop-Sqoop

This project is using HDFS along with Sqoop using MySQL query.

Sqoop import the data from MYSQL to HDFS and stores as textfiles as result.
Data are modified using MySQL select statement, allow us to optimize our result.

The resulting directory for the Sqoop Import should not be exist prior running the command, 
the sqoop query will respondible for creating each directory.

These queries can be saved as sqoop jobs:

Sqoop job commands:

           create sqoop job: 
           sqoop job --create --import --connect jdbc:mysql://example.com/db {your remaining import query goes here}

           list sqoop job: 
           sqoop job --list -meta-connect jdbc:hsqldb:hsql://localhost:16000/sqoop

           kill sqoop job:
           sqoop job --kill __ -meta-connect jdbc:hsqldb:hsql://localhost:16000/sqoop
           
           run sqoop job
           sqoop job --meta-connect jdbc:hsqldb:hsql://localhost:16000/sqoop --exec BranchJob
           
If the sqoop job is created and running on sqoop metastore, make sure the sqoop metastore is running when the sqoop job is executing.
