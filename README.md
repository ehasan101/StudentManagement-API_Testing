# API_Testing-Project
<br>

## API Testing: Student-Management with Postman
The Student Management API for managing student records. This Postman project covers the end-to-end testing of its core functionalities, from creating a new student to deleting their records. The tests are built to verify the API's logic, response accuracy, and status codes. It's evaluating the APIs are working functionality and usability as expected. 


## Exploring My Testing Process: A Video Walkthrough!
> [<img src="https://img.youtube.com/vi/PtrbE-uaC18/hqdefault.jpg" width="700" height="480"/>](https://www.youtube.com/embed/PtrbE-uaC18)


## How to run this project!
1. Install [Postman](https://www.postman.com/).
2. Install [Node.js](https://nodejs.org/en/).
3. Download [Project file](https://drive.google.com/drive/folders/16SzJWDvhETXTYWBwDAOiL40Y8HVhyf8E?usp=sharing).
4. Now Import collection & environment file into **Postman**: \
`file > import > choose the method > press 'import'`
5. Run Desired API request 

**Run on cmd**
1. Open cmd on project folder or move to project folder `cd Downloads/project_file`
2. Run the follwing command 
Install newman `npm install -g newman`
3. Now 
`newman run Student_Management.postman_collection.json -e Std_Manage.postman_environment.json`
4. **If want to export test results** \
   first install them \
   `npm install -g newman-reporter-html` \
 and `npm install -g newman-reporter-htmlextra`
6. Now run follwing command for report \
`newman run Student_Management.postman_collection.json -e Std_Manage.postman_environment.json -r cli,htmlextra`

## HTTP Status Codes
HTTP status code are 3 digit number which a server response to a browser’s request.
Those are divided into 5 categories.
```JavaScript
1xx - Informational Purpose
2xx - Success
3xx - Redirection
4xx - Client Errors
5xx - Server Errors
```
![http_status_code](https://drive.google.com/uc?export=view&id=1iwy6FJw2krnOtpOmMhhHocFpXgfguTBM)

<br>

## Working Scenarios & What I have done in this Testing!
This project is designed to test the complete lifecycle of a student record in the database through a series of chained API requests.
The collection follows a logical sequence to ensure data integrity and proper API functionality:
* Create a New Student: A POST request is sent with student details to create a new record.
* Validate Creation: The studentId from the creation response is automatically extracted and saved to an environment variable.
* Retrieve & Verify: GET and PUT requests use this studentId to fetch, verify, and update the newly created record.
* Clean Up: A DELETE request uses the same studentId to remove the student record from the database, ensuring the test is self-contained.

**Essential Testing Strategies:**
* Dynamic ID Chaining: I used Postman's scripting capabilities to capture the studentId from the POST response and automatically pass it to subsequent GET, PUT, and DELETE requests. This makes the test dynamic and reusable.
* Comprehensive Assertions: For each request, I have written multiple tests in the "Tests" tab to validate:
* HTTP Status Codes: Ensuring the API returns correct codes (e.g., 201 Created, 200 OK).
* Response Time: Checking that the API responds within an acceptable performance threshold (e.g., under 1000ms).
* Response Body Content: Verifying that the data returned in the response body is accurate and matches the data sent in the request (e.g., confirming the first_name is correct after creation and updates).





## Test Report with Newman :
A Newman report has been generated for the API test
#### 1. HTML Format: [_Report Link_](https://drive.google.com/file/d/1JfJc_MrPVi20NrA6aBR1WLUjBHF8XCvt/view?usp=drive_link)

#### 2. Snapshots of Report:
> * **Summary Report**
![Summary_1](https://drive.google.com/uc?export=view&id=17KXS5vg5di8ESAGu2cqywAhsd2LLNtmZ)
![Summary-2](https://drive.google.com/uc?export=view&id=1R3yo4u3Mv_TI1C0c6Bfge1go1LdySIpf)

> * **Total Requests**
![Total_1](https://drive.google.com/uc?export=view&id=1oz3USCQ2x2haoVNQQcsjF15aqdxRAhtl)
![Total_2](https://drive.google.com/uc?export=view&id=1zAM1MgTditIjCPQ4zKCR43r-mdmnUZnU)

> * **Failed Requests**
![Failed](https://drive.google.com/uc?export=view&id=1_sXJlXLexn6buN6153Cx5S1y_nVa6Btb)

---
|:warning: **if you face any type of image broken/missing issue, please `refresh` this web page again.**|
| --- |

### **#Happy_Testing**
---

