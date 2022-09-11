---
layout: single
title:  "Introduction to DBMS"
comments: true
summary: "Introduction to DB and DBMS"
categories: [DBMS]
tags: SQL
toc: true
author_profile: false

---

The DBMS tutorials are based on the course <i>LE/EECS3421: Introduction to Database Systems</i> offered at York University. The course was conducted in the 2022-2023 fall semester by Dr. Habib-ur Rehman.

## Database
Database is a collection of data. It does not depend on the format of the data sets, where it is stored and the size of the data sets.
It can be a single file or multiple files.
For example, a csv file containing data is also a database.

## Database Management System
What happens if the data in the database needs to be created, updated, deleted or read frequently? It would be good to have a system to manage the collections of data.
DBMS stands for Database Management Systems. The system is developed to manage the database efficiently. The DBMS software serves the interface for the functions.
For example, Peoplesoft and SAP are DBMS used for HR applications. As applications handle sophisticated tasks and store a big amount of secured data such as bank transactions, the developers separate the tiers of the applications based on its functionality and purpose. Let's first take a look at the Two Tier Application Architecture.

<p align="center">
  <img src="../../assets/images/DBMS/two-tier.png" alter="two-tier-architecture">
</p>


The application tier is concerned with the user interface and the business logic (functionality). The DB tier takes care of the data. You can develop your own software for DBMS or buy it. The two components do not strongly depend on each other. Therefore, you have more options to choose software to manage your database as needed. However, the programming language for both tiers should be the same for the integration. 

<br>
The application tier receives meta-data from the users and tosses the data to the DB tier. Meta-data is also called schema because it defines the data field. Let's say we have a log-in application. The inputs we expect from the users are a username, a password and a security answer. These inputs are specific to the log-in application. If we have a student management application, the inputs would be different. This is mini-world.
The inputs of the log-in application need are stored in DB in a structured manner and this is meta-data. Therefore, the meta-data is dependent on the application. 

<p align="center">
  <img src="../../assets/images/DBMS/db-env.png" alter="db-system-environment">
  courtesy: R. Elmasri and S. B. Navathe
</p>

Each data has a type. For instane, the username is a string and the password is an integer. The information about the types of the meta-data, where to store, and how to handle, etc are stored in the stored database (Fig.1.1).


## Data Model
The meta-data is stored in a structured manner. But how do we structure the data?
There are a couple of ways to do this. The relational data model uses SQL language and the non-relational data model uses No-SQL. In this tutorial, we will focus on the relational data model. For that, we will use MySQL which is a software system for relational DBMS. We need to download MySQL community server and a workbench.
To download, please click this [link](https://dev.mysql.com/downloads/).

## Challenge
When we handle data using DBMS software, there is a challenge we need to consider.
What if multiple users try to change the data? Suppose a scenario where a student uploads a file and a teacher deletes the submission immediately. How does the DBMS handle the situation? Also, what if we want to display different user interfaces to users with different roles? One thing to keep in mind is that DB should remain consistent. We will discuss how to develop such DBMS that is consistent and secured through out the posts. 



