### SSE Assignment

#### Rahul M Menon
#### CB.SC.P2CYS23015

### Case study : Corporate HRMS System
#### Define the Scope and Objectives

#### Scope
•	A corporate HRMS system where employes can log in ,view account details, Change the database, apply leave.

#### Objectives
•	Identify potential threats
•	Asses the impact and likelihood of threats
•	Develop mitigation strategies

#### Entities
•	Employee (External Entity)
•	Web Server (Process)
•	Database Server (Data Store)
•	Authorization Server (Internal Entity)

 Click on new model

 ![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/d8695e78-edc9-4b23-92f0-73c7cf70f89c)


Now the resultant canvas will be :
Demo of Simple Web Application

 ![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/d836b7c2-b109-4baf-98af-b6f3e39118b5)

Identify And Analyse Threats:
Navigate to ‘View’ and click ‘analysis view’

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/e7877c37-7a24-4aa7-a660-c003ce5d1cd7)

The Data Flow sequence will be

Employee -> Web Application (Submit credentials)
o	Data Flow Type: HTTP
o	Description: Employee submits login credentials to the web application.

Web Application -> Authorization Server (Verify credentials)
o	Data Flow Type: HTTPS
o	Description: The web application sends the credentials to the authorization server for verification.

Authorization Server -> Web Application (Send account details)
o	Data Flow Type: HTTPS
o	Description: The authorization server sends the account details back to the web application.

Web Application -> Employee (Display account details)
o	Data Flow Type: HTTP
o	Description: The web application displays the account details to the customer.

Employee -> Web Application (Request Applying Leave)
o	Data Flow Type: HTTPS
o	Description: The employee requests a applying leave through the web application.

Web Server -> Authorization Server (Update Leave Account)
o	Data Flow Type: HTTPS
o	Description: The web server sends the leave request to the authorization server to update the leaves.

Web Server -> SQL Database Server(Initiate request for Update)
o	Data Flow Type: HTTPS
o	Description: The web server initiates the request with the database server

SQL Database Server -> Web Server (Confirm Update)
o	Data Flow Type: HTTPS
o	Description: The SQL Database Server confirms the update and sends the confirmation back to the web server.

Web Server -> Employee (Display HRMS System)
o	Data Flow Type: HTTPS
o	Description: The web server displays the leave status to the employee in HRMS System

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/a71cf413-d191-4111-82b1-e9cdfa983b59)

Analysis View

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/f8d0cf51-091e-4e4c-87dd-93ccbee698c0)

We select a specific threat and check its properties

![image](https://github.com/RahulMMenon011/Secure-System-Engineering/assets/140642506/525594e3-bbf5-4293-a757-58c420a6aec0)



