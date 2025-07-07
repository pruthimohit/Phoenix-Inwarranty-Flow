# Postman API Automation Integration with Github Actions #

This repository is a demonstration for POC for integrating postman tests with github actions. The tests are written in postman and they are executed on the VM with the help of Newman-reporter-htmlextra.
Github Actions will trigger the project executions on every push to the main branch. You can also execute the project manually using workflow_dispatch. The project runs on a scheduled time with the help of a cron job.

The HTML report is archieved and kept in the artifact section for the team to download it. Along with that they can view the report directly from the github page : https://pruthimohit.github.io/Phoenix-Inwarranty-Flow/
The latests report is mailed to the team members using gmail SMTP.

## About Me ##
Hi My Name is Mohit Pruthi. I've 5+ years of experience in Automation Testing. My skillset includes UI Automation with Selenium Webdriver, Cypress, Playwright and for API Testing I use Rest Assured and Postman.
You can connect with me over: https://www.linkedin.com/in/mohitpruthi/

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge case Testing
3. Token Testing
4. Data Driven Testing with csv
5. Schema Validation
6. Secrets Management with Github Secrets 

## Tech Stack ##
1. Postman
2. Nodejs v22
3. Newman
4. Newman-Reporter-htmlextra
5. Github Actions
6. gmail SMTP
7. Github Pages
8. CSV for Data Driven Testing
9. AWS-EC2 instance for self hosted github runner.

## Github Pages ##
You can directly view the latest test report of Postman Test at the Github Page link : https://pruthimohit.github.io/Phoenix-Inwarranty-Flow/

## HTML Report ##
The Report will be created in the newman folder

<img width="284" alt="image" src="https://github.com/user-attachments/assets/24257e44-0d7d-4529-b3f5-d3a8f1114a85" />

## Project Structure ##
```
Phoenix In-warranty Flow
├─ Inwarranty-flow Collection Copy.postman_collection.json # Collection File
├─ QA.postman_environment.json # ENvironment File
└─ testData.csv # TestData File
```
## How to run the Project? ##
You can run the project on your local system for that :
1. Clone the Project on local System : https://github.com/pruthimohit/Phoenix-Inwarranty-Flow.git
2. Install Nodejs and NPM from https://nodejs.org/en
3. Install Newman using ``` npm install -g newman ```
4. Install Newman-reporter-htmlextra using ``` npm install -g newman-reporter-htmlextra ```
5. Run the Newman Command: ```
newman run 'Inwarranty-flow Collection Copy.postman_collection.json' \
-e QA.postman_environment.json \
-r cli,htmlextra \
--reporter-htmlextra-export ./newman/index.html```
