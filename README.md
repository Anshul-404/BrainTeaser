# BrainTeaser Application

The BrainTeaser Application is a Java desktop solution designed to simplify exam management for teachers and empower students with easy access to their performance insights.

![Splash Screen](images/SplashScreen.png)

## Features

- **Admin Panel:**
  - Teachers can easily create exams on various subjects, edit papers, register students, and view their scores.

- **Data Security:**
  - The application ensures data security through robust measures, including MD5 encryption.

- **Student Panel:**
  - Students have the ability to take tests, view exam scores, and change their passwords.

## Overview

The BrainTeaser Application is a Java desktop application that streamlines the process of exam creation, resulting in a significant reduction in exam creation time compared to traditional manual methods. It utilizes an SQL database to store exam questions, student accounts, and results, ensuring efficient data management.

To protect sensitive data, BrainTeaser employs robust security measures, including MD5 encryption and access controls, maintaining the confidentiality of exam-related information.

A key feature of the application is its student-centric approach. It enables students to easily access and review their past exam results, leading to a decrease in inquiries to teachers regarding grades.

The application consists of two panels - the Admin panel for teachers and the Student panel for students. In the Admin panel, teachers have access to comprehensive exam management functionalities, allowing them to create and manage exams effortlessly.

BrainTeaser empowers educators with efficient exam management, providing a comprehensive platform for teachers to streamline their exam creation process. Simultaneously, the Student panel offers students convenient access to their exam scores and password management, fostering a seamless learning experience.


## Database Configuration


### IMPORTING DATABASE:

* Copy "brainteaser.dmp" file to bin folder of your system's Oracle directory.

* Use the following commands on Oracle SQL

```
create user quiz identified by quiz
grant resource,connect,dba to quiz
```

* Use the following commands on Command Prompt (Administrator) -


```
cd path/to/oracle/bin/
imp quiz/quiz

Import data only (yes/no): no > no

Import file: EXPDAT.DMP > brainteaser.dmp

Enter insert buffer size (minimum is 8192) 30720> 30720

Export file created by EXPORT:V11.02.00 via conventional path

Warning: the objects were exported by GROCERY, not by you

import done in WE8MSWIN1252 character set and AL16UTF16 NCHAR character set
import server uses AL32UTF8 character set (possible charset conversion)
List contents of import file only (yes/no): no > no

Ignore create error due to object existence (yes/no): no > no

Import grants (yes/no): yes > yes

Import table data (yes/no): yes > yes

Import entire export file (yes/no): no > yes
```

### ADMIN DETAILS: ###


<details>
  <summary>Default Credentials For Admin Login</summary>
  <p>User ID : anshul@007</p>
  <p>Password : password</p>
</details>

* To create a new admin user, first generate a MD5 hash of your password [here](https://codebeautify.org/md5-hash-generator) in uppercase.

### Run these commands on Oracle SQL -

```
connect quiz/quiz
insert into users values ('your@userid', 'YOUR_HASH_IN_UPPERCASE', 'Admin');
commit;
```
### To Remove Default Credentials, run these commands on Oracle SQL -

```
connect quiz/quiz
delete from users where USERID = 'anshul@007';
commit;
```

## How to Use

To use the BrainTeaser Application, follow these steps:

1. Clone the GitHub repository.
2. Launch the .jar file
3. Use the Admin panel for exam creation, student registration, and score management.
4. Use the Student panel for taking tests, viewing exam scores, and changing passwords.

## Requirements

- Java Runtime Environment (JRE) 1.8 or later.
- SQL Database (OracleSQL).

---
