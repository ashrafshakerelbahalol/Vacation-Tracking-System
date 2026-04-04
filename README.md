# Vacation-Tracking-System
# vision
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
  making logging: allow system to save log files to use it to backup when failure happen
  
## Non-functional requirement:
 1- Availability makes the system available 24/7
 
 2-Scalability allows multiple user to interact
 
 3-Security: make the system secure against cyber attacks
 
 4- Ease of Use: The system must be intuitive, intelligent, and easy to use
  
# Constraints:
  use existing hardware,middleware
  
  Use sso
  
  Integrate with legacy hr system

# Domain Problem 
  For many businesses today, the independence of workers has been ever 
  increasing. It is not uncommon for workers to divide their time across multiple projects and to report to multiple project managers. As a result, 
  managers have fewer informal interactions with their workers and find it 
  increasingly difficult to be aware of and manage their workers’ vacation time.
  
# Actors:
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
            
# Employee
  <img width="541" height="1181" alt="Untitled Diagram drawio" src="https://github.com/user-attachments/assets/3b003d3f-83cd-40de-b8c9-a211ac4d3692" />
  
# Manager
  <img width="332" height="752" alt="Manager" src="https://github.com/user-attachments/assets/780055bc-5f8b-4439-8b2e-cea6f5d144ab" />

