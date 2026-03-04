# Postman API Automation integration with Github actions #

This repository is a demonstration for POC for integrating postman tests with github actions.Thes tests are written in postman and they are executed in the VM with the help of newman and newman reporter html extra.
The github action trigger the project execution on push to the main branch.You can also execute the project manually using the workflow_dispatch.Tge project executes in a scheduled time with the help of cron job.
The HTML report is archieved and kept in the artifact section for the team to download along with that they can view the report directly from the github page:https://varsha8108.github.io/Inwarrantyflow/
The latest report is mailed to the team members using gmail smtp
# About me #
My name is Varsha, i have overall of 9.5 years of experience in Automation and functional testing, and my skillsets includes Automation with selenium, API testing with Postman and restassured, You can connect with me on linkedin: https://www.linkedin.com/in/varsha-krishnakumar-bb356334/
# Tech stack #
1. Postman
2. Node js v22
3. Newman
4. Newman-reporter-HTML extra
5. gmail smtp
6. github actions
7. csv for data driven testing
8. AWS ec2 for self hosted github runner
9. github pages

# github pages#
You can view the latest report of postman test at the github page link:https://varsha8108.github.io/Inwarrantyflow/
# HTML report#
The HTML report will be created in the newman folder
![Postman report](https://github.com/varsha8108/Inwarrantyflow/blob/static-content/Screenshot%202026-03-04%20160848.png)

# Project structure #
Inwarrenty flow
├─ In warrantyflow CSV_Data.postman_collection.json # Collection file
├─ newman
├─ QA.postman_environment.json # Environment file
└─ Testdata.csv # Test data file

# Test coverage#
1. Positive test cases
2. Negative test cases
3. Token test cases
4. Data driven test case with CSV
5. schema validation
6. secrets management with github coverage

# How to run the project#
You can run the project on the local system for that 
1. clone the project on local system: https://github.com/varsha8108/Inwarrantyflow
2. Intall node js at https://nodejs.org/en/download/current
3. Install newman $ npm install -g newman
4. Install newman - reporter-htmlextra : $ npm install -g newman-reporter-htmlextra
5. Run the newman command
               newman run "In warrantyflow CSV_Data.postman_collection.json" \  
              -e QA.postman_environment.json \
              -d Testdata.csv \
              -r cli,htmlextra \



