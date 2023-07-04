# Claim Portal Project Assignment for Sun Venture

## Introduction
This is a simple project to demonstrate internal expense claim submission and approval. This project was built based on the technology stack as per below:
  - React (including Axios, Semantic UI, Webpack, NodeJS, Route) 
  - Spring Boot (including MVC, JPA, REST data, Maven)
  - H2 Database
ReactJS frontend will interact with the users and make REST api call via Spring REST endpoints using JSON data format.

## Installation & Configuration
### For Frontend : 
1. clone '**react-frontend**' project to your local machine and unzip
2. cd to project folder
3. run `npm install`
4. run `npm start`
Note: You should have port **3000** avilable for running this project
### For Backend : 
1. clone '**springboot-backend**' project to your local machine and unzip
2. cd to project folder
3. run `mvn clean`
4. run `mvn compile`
5. run `mvn exec:java`
Note: You should have port **8080** avilable for running this project
### For Database : 
There is no requirement for DB setup. Spring configuration will automatically create tables upon succesfully run the project. 
The database file is bundled as dependency into this project via Spring H2 and JPA and it is located inside project folder (*.db file)

## Scope of functionalities 
#### 1. Login Module

   - Able to redirect user to different view for different user role (i.e., manager view and employee view)
   - Error message propmt upon login failure
   - Hardcode login credential for testing purpose.
       * Employee 1 => user id: 101 / password: 101
       * Employee 2 => user id: 102 / password: 102
       * Manager 1 => user id: 401 / password 401
         
![image](https://github.com/joebkk/claim-portal/assets/64820995/414e7e81-9f43-4886-99ea-2cdd314db5f7)

#### 2. Employee View
   - Able to track all the submitted claims that only belong to the login user (User 101 is not able to view claims from user 102)
   - Able to raise a new claim request via claim form modal (popup)
   - Able to raise claim request to different reporting managers
   - Able to see claim request reflect immedialtely after submitted 

![image](https://github.com/joebkk/claim-portal/assets/64820995/05673af5-4050-4cc0-a211-7957bb4be3a6)
![image](https://github.com/joebkk/claim-portal/assets/64820995/25a2457c-3ded-4886-bd2f-81051ae63798)

#### 3. Manager View
   - Able to see all claims that have been raised to him/her from multiple employees
   - Able to approve/reject each claim indiviually
   - Able to see status changed immedialtely upon approve/reject
     
![image](https://github.com/joebkk/claim-portal/assets/64820995/d25de09c-6f2a-4d0e-bafb-35c5b031645e)

## Area of improvement
- Add filter, column sorting, paging, and searching functionality for claim table
- Add feature for bulk approval/reject
- Implement full-fledged login validation
- Refactor soure code
  
## Note
Any feedbacks or comments are most valued and always welcome!
