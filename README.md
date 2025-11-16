# Postman API Automation Integration with Github Actions #

This repository is demonstration for POC for integrating postman tests with github actions. The tests are written in postman and they are executed on the virtual machine with the help of newman and newman-reporter-htmlextra.
Github actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The project runs on a scheduled time with the help of corn jobs.

The HTML report is archieved and kept in the artifact section for the team to download it. Along with that they can view the report directly from the github page: https://gauravjangde.github.io/Phoenix-Inwarranty-Flow/.
The latest report is mailed to the team members using GMAIl SMTP.

## About Me ##
Hi, My Name is Gaurav Jangde. I have 12 years of experience in Manual and Automation Testing. My Skillset includes UI Automation using Selenium Webdriver and Java, and for API Testing I use Rest Assured and Postman.
You can connnect with me over: https://www.linkedin.com/in/gaurav-jangde29/

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets Management with Github Secrets

## Tech Stack ##
1. Postman
2. NodeJS 22v
3. Newman
4. Newman-Reporter-Htmlextra
5. Github Actions
6. Gmail SMTP
7. Github pages
8. CSV for Data Driven Testing
9. AWS-E2 instance for self hosted github runner.

## Github pages ##
You can directly view the latest test report of the Postman Test at the Github Page Link : https://gauravjangde.github.io/Phoenix-Inwarranty-Flow/

## HTML Report ##
The Report will be created in the newman folder
![Postman Report](https://github.com/GauravJangde/Phoenix-Inwarranty-Flow/blob/static-content/Newman%20HTML%20Report.png)

## Project Structure ##
```
Phoenix Inwarranty Flow
├─ InWarrenty Flow APIs Copy.postman_collection.json #Collection file
├─ QA.postman_environment.json #Environment file
└─ testData.csv #Test data file
```

## How to run the project? ##
You can run the project on your local system for that:
1. Clone the project on Local system: https://github.com/GauravJangde/Phoenix-Inwarranty-Flow.git
2. Install NodeJs and NPM from [https://nodejs.org/en](https://nodejs.org/en)
3. Install Newman using npm install -g newman
4. Install Newman-reporter-htmlextra using npm install -g newman-reporter-htmlextra
5. Run the Newman comment:
             newman run 'InWarrenty Flow APIs Copy.postman_collection.json' \
             -e QA.postman_environment.json \
             -d testData.csv \
             -r cli,htmlextra \
             --reporter-htmlextra-export ./newman/index.html

