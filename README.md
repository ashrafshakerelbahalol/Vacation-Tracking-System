# Vacation-Tracking-System
## vision
A Vacation Tracking System (VTS) will provide individual employees with the 
capability to manage their own vacation time, sick leave, and personal time off, 
without having to be an expert in company policy or the local facility’s leave 
policies.The underlying motivations for this desire include 
the need to streamline the functions of the human resources (HR) department, to 
minimize noncore, business-related activities of management, and to give a sense 
of empowerment to the employees.
##Functionial Requirement
  Manage Time: vacation request can add edit view request 
  Approve Request: Describes how a manager responds to a subordinate’s request for vacation time. 
  Award Time: Describes how a manager can award a subordinate extra leave time (comp time).
  Manage Leave Categories: Describes how an HR clerk manages leave categories and their rules.
  Override Leave Records: Describes how an HR clerk may override any rejection of leave time requests made by the rules in the system.
  making logging: allow the system to save log files to use them to back up when failures happen
  
## Non-functional requirement:
 1- Availability makes the system available 24/7
 
 2-Scalability allows multiple user to interact
 
 3-Security: make the system secure against cyber attacks
 
 4- Ease of Use: The system must be intuitive, intelligent, and easy to use
  
## Constraints:
  use existing hardware,middleware
  
  Use sso
  
  Integrate with legacy hr system

## Domain Problem 
  For many businesses today, the independence of workers has been ever 
  increasing. It is not uncommon for workers to divide their time across multiple projects and to report to multiple project managers. As a result, 
  managers have fewer informal interactions with their workers and find it 
  increasingly difficult to be aware of and manage their workers’ vacation time.
  
## Actors:
   Employee: The main user of this system. An employee uses this system to 
            manage his or her vacation time. 
            
   Manager: An employee who has all the abilities and goals of a regular 
            employee, but with the added responsibility of approving vacation requests 
            for immediate subordinates. A manager may award subordinates comp 
            time, subject to certain limits set in the system.
            
   Clerk: A member of the HR department who has sufficient rights to view 
            employees’ personal data and is responsible for ensuring that employees’ 
            information in all HR systems is up to date and correct. An HR clerk can 
            add or remove nearly any record in the system. In the real world, HR clerks 
            may or may not be employees; however, if they are employees, they use two 
            separate login IDs to manage these two different roles.
            
   System Admin: A role responsible for the smooth running of the system’s technical resources 
            (e.g., Web server, database) and for collecting and archiving all log files

## Data model
Employee,
Manager,
Vacation Request,
Category of Vacation

<img width="321" height="241" alt="ClassUML" src="https://github.com/user-attachments/assets/b2607ae7-a2f9-4310-90f1-72685e7dc50e" />

            
## Flow Chart     

### Manage Time :- Employee flow 
  <img width="541" height="1181" alt="Untitled Diagram drawio" src="https://github.com/user-attachments/assets/3b003d3f-83cd-40de-b8c9-a211ac4d3692" />
  
### Manage Time :- Manager flow
  <img width="332" height="752" alt="Manager" src="https://github.com/user-attachments/assets/780055bc-5f8b-4439-8b2e-cea6f5d144ab" />

# Sequence Diagram  Manage Time
<img width="851" height="1012" alt="Employee create request" src="https://github.com/user-attachments/assets/cbe7a7f8-86d8-4998-92fc-cacf2c74a04a" />

# Pseudocode:   Manage Time

 PROCEDURE ProcessEmployeeRequest()
 
    Employee inputs Credentials to VTS
    
    VTS authenticates the employee
    
    VTS returns "View all requests dedicated to the user" to the employee
    
    Employee sends "Create new request" command to VTS
    
    VTS returns a new request page  to the employee
    
    Employee fills in the required info and submits RequestData to VTS
    
    IF RequestData is NOT VALID THEN
    
        VTS returns "error msg with explanation" to the employee    
        
    ELSE IF RequestData is VALID THEN
    
        VTS  save request with pending approval   
        
        VTS sends the command "send email to" to the Email Server
        
        The email server sends an email to the manager
        
        Email Server returns "confirm sending email" to VTS
        
        VTS returns "show request as pending approval to the employee     
        
    END IF

END PROCEDURE

# Task Part 2:

## UI

### UI (Employee)
<img width="1080" height="592" alt="Screenshot 2026-04-11 134858" src="https://github.com/user-attachments/assets/3d4004fe-f701-4da7-a434-591597029e79" />

### UI (Manager)
<img width="1154" height="630" alt="Screenshot 2026-04-11 143125" src="https://github.com/user-attachments/assets/80e11e39-ef05-4888-bfcd-0e73cb740443" />


## Adding a layer of hr approval or pending
To ensure minimum impact when adding new statuses, we will decouple the request logic from the status logic using the State Pattern. This allows us to treat each status as a plugin. If the business decides to add an HR approval layer, we simply plug in the new 'HR_Pending' state and update the transition rule, leaving the original Employee and Manager code completely untouched

## Flow Chart
### Withdraw request
  <img width="271" height="932" alt="Withdraw request" src="https://github.com/user-attachments/assets/d78a2674-628a-461f-bc66-a68590d6cd14" />

### Cancel Request
  <img width="320" height="1282" alt="cancel Request" src="https://github.com/user-attachments/assets/ab48345b-36bf-487d-91df-9695c6a83ad4" />
  
### Edit request
  <img width="362" height="1161" alt="Edit request" src="https://github.com/user-attachments/assets/a559b63e-ed53-4e69-99b5-437cca9d7402" />
  
## Sequence Diagrams
### Edit request
![hgh](https://github.com/user-attachments/assets/20734078-1ef4-4399-ac98-578fc0c4d46d)
### Cancel Request
<img width="829" height="770" alt="cancel request sequence drawio" src="https://github.com/user-attachments/assets/bb6d2738-0bb4-4936-98a4-582024b90c3d" />




