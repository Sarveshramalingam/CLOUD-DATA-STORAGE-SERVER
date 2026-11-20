# CLOUD-DATA-STORAGE-SERVER

### NAME : Sarvesh R
### REG NO: 212225100045

## Aim

To create and configure an Amazon Relational Database Service (Amazon RDS) instance as a cloud data storage server, configure the required security settings, connect it to a web application, and perform database operations using the application.

## Algorithm / Steps

1. Create a Security Group for the RDS database.
2. Add an inbound rule to allow MySQL (Port 3306) access from the Web Security Group.
3. Create a DB Subnet Group using two Availability Zones.
4. Launch an Amazon RDS MySQL database instance.
5. Configure the database with the required identifier, username, password, storage, and instance class.
6. Associate the database with the created Security Group and Subnet Group.
7. Wait until the database status becomes **Available**.
8. Copy the RDS endpoint.
9. Open the web application using the provided Web Server IP address.
10. Enter the RDS endpoint, database name, username, and password.
11. Connect the application to the database.
12. Verify the connection by adding, editing, and deleting records in the Address Book application.


## Program

### Security Group Configuration

* Security Group Name: **DB Security Group**
* Inbound Rule: **MySQL/Aurora (3306)**
* Source: **Web Security Group**

### DB Subnet Group

* Name: **DB-Subnet-Group**
* VPC: **Lab VPC**

### Amazon RDS Configuration

* Engine: **MySQL**
* Template: **Dev/Test**
* Availability: **Multi-AZ**
* DB Instance Identifier: **lab-db**
* Username: **main**
* Password: **lab-password**
* Instance Class: **db.t3.micro**
* Storage: **20 GB (General Purpose SSD)**

### Connect the Application

```text
Endpoint : <RDS Endpoint>
Database : lab
Username : main
Password : lab-password
```

After submitting the above details, perform Add, Edit, and Delete operations on the Address Book application.

## Output
<img width="1920" height="1080" alt="Screenshot (198)" src="https://github.com/user-attachments/assets/f440069f-d11b-41c2-9663-104416b8b99d" />
<img width="1920" height="1080" alt="Screenshot (199)" src="https://github.com/user-attachments/assets/3bb7e03e-87b3-457a-86ac-ebd6b2438c86" />
<img width="1920" height="1080" alt="Screenshot (200)" src="https://github.com/user-attachments/assets/949e0eb6-0013-4b9e-aa1f-0255265b5dca" />
<img width="1920" height="1080" alt="Screenshot (201)" src="https://github.com/user-attachments/assets/f6feb463-3215-4de7-b2db-b3dd89dc76c0" />
<img width="1920" height="1080" alt="Screenshot (202)" src="https://github.com/user-attachments/assets/5d52f76c-7e91-4324-a767-a2e984c5bebd" />
<img width="1920" height="1080" alt="Screenshot (203)" src="https://github.com/user-attachments/assets/e77721fb-714b-4e9b-871a-9a59c36e3b6e" />
<img width="1920" height="1080" alt="Screenshot (204)" src="https://github.com/user-attachments/assets/96239b59-fa7e-47a1-a4ad-55f2dc578084" />
<img width="1920" height="1080" alt="Screenshot (205)" src="https://github.com/user-attachments/assets/e03bed47-6ff9-4ef0-807a-2bf3e9823b31" />
<img width="1920" height="1080" alt="Screenshot (206)" src="https://github.com/user-attachments/assets/521ae0d6-ea1d-4b45-9ffc-dd1776ff5cda" />



## Result

Thus, an Amazon RDS database instance was successfully created and configured as a cloud data storage server. The database was securely connected to a web application, and data operations such as inserting, updating, and deleting records were successfully performed through the application.


