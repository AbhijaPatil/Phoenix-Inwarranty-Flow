# Postman API Automation Integration with Github Actions #

This repository is a demonstartion for POC for Integrating Postman tests with Github Actions. The tests are written in Postman and they are executed on the virtual machine with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The Project runs on the scheduled time with the help of the cron job.

The HTML reports is archieved and kept in the artifact section for the team to download it. Along with that they can view the report directl from the github page: https://abhijapatil.github.io/Phoenix-Inwarranty-Flow/.
The latest report is mailed to the team members using GMAIL SMTP.

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets management with Github Secrets 

## Tech Stack ##
1. Postman
2. Nodejs 22v
3. Newman
4. Newman-reporter-htmlextra
5. Github Actions
6. Gmail SMTP
7. Github Pages
8. CSV for Data Driven Testing
9. AWS-EC2 for self hosted github runner.

## Github Pages ##
You can directly view the latest test report of the Postman Test at the Github Page Link: https://abhijapatil.github.io/Phoenix-Inwarranty-Flow/

## HTML Report ##
The report will be created in the newman folder
![Postman Report](https://github.com/AbhijaPatil/Phoenix-Inwarranty-Flow/blob/static-content/Newman_Report.png)

## Project Structure ##
```
Phoenix-Inwarranty-Flow
├─ In warranty-flow Collection.postman_collection.json #Collection File
├─ QA.postman_environment.json #Environment File
└─ testdata.csv #TestData File

```

# How to run the Project #
You can run the project on your local system for that 
1. Clone the project on your Local System: https://github.com/AbhijaPatil/Phoenix-Inwarranty-Flow.git
2. Install Nodejs and NPM from https://nodejs.org/en
3. Install Newman using ``` npm install -g newman ```
4. Install Neman-reporter-htmlextra using ``` npm install -g newman-reporter-htmlextra ```
5. Run the newman command:
   ```
              newman run 'In warranty-flow Collection.postman_collection.json' \ 
             -e QA.postman_environment.json \
             -d testdata.csv \
             -r cli,htmlextra \
             --reporter-htmlextra-export ./newman/index.html
   ```









    
