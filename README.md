# API_Testing-Project
<br>

## API Testing for Student-Management with Postman
This project is on API testing with Postman for the Student Management web-service. It's evaluating the APIs are working functionality and usability as expected. 

## How to run this project!
1. Install [Postman](https://www.postman.com/).
2. Install [Node.js](https://nodejs.org/en/).
3. Download [Project file](https://drive.google.com/drive/folders/16SzJWDvhETXTYWBwDAOiL40Y8HVhyf8E?usp=sharing).
4. Now Import collection & environment file into Postman: \
`file > import > choose the method > press 'import'`
5. Run Desired API request 

Run on cmd
1. Open cmd on project folder or move to project folder `cd Downloads/project_file`
2. Run the follwing command 
Install newman `npm install -g newman`
3. Now 
`newman run Student_Management.postman_collection.json -e Std_Manage.postman_environment.json`
4. If want to export test results first install them \
   `npm install -g newman-reporter-html` \
 and `npm install -g newman-reporter-htmlextra`
6. Now run follwing command for report \
`newman run Student_Management.postman_collection.json -e Std_Manage.postman_environment.json -r cli,htmlextra`



