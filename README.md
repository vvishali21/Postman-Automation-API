# Postman-Automation-API

Step 1: import this in environments global 

           API automation.postman_environment.json       


Step 2: import this in collections

           Category.postman_collection.json






           ENVIRONMENTS
           
1.	Define the Environment Variables:
 
•	In the "Manage Environments" dialog, you can create a new environment or select an existing one.

•	Define the environment variables, including the "baseUrl" You can name the variable as "baseUrl" and set its value to the URL of your API.

3.	Use the Base URL Variable in Requests:

•	In your requests, you can reference the "baseUrl" variable by using double curly braces, like {{baseUrl}}.

•	For example, if your "baseUrl" variable is set to "http://localhost:8001/api" you can use it in your requests like this: {{baseUrl}}/endpoint.




Postman Automation and Report Generation
1. Setting up Postman
If you haven't already, download and install Postman. Postman offers both a web-based platform and a desktop application.

2. Creating Automated Tests
Import or Create Collections: You can import existing API requests or create new collections within Postman.
Create and Configure Environment Variables: To ensure flexibility and reusability, set up environment variables for your tests, such as base URLs, authentication details, and common data.
Write Test Scripts: In Postman, you can write test scripts using JavaScript. These scripts will validate the responses from your API endpoints.
Automate Using Newman: Postman provides multiple options for test automation. You can use Postman Monitors for cloud-based automation or Newman, the command-line runner, for local execution.

3. Report Generation
newman
Once you've successfully installed Node.js, the next step is to install Newman on your machine. To do this, use the following command:
npm install -g newman

Install custom reporter
Newman Reporter HTML Extra is an external reporter for Postman's Newman, which is a command-line collection runner for Postman, a popular API testing tool. Newman allows you to run Postman collections from the command line, making it easier to integrate API testing into your CI/CD pipelines or scripts.
The Newman Reporter HTML Extra is an extension of the default HTML reporter for Newman, and it provides additional features and customizations for generating more detailed and attractive HTML reports after running Postman collections.

To enhance Newman's capabilities and generate more detailed reports, you can extend it with the "newman-reporter-htmlextra" package. This extension allows for the separation of iteration runs and provides additional helpers for creating customized templates.
npm install -g newman-reporter-htmlextra

To execute your API tests via the command line with the enhanced reporting, use the following command:
newman run Category.postman_collection.json e "API automation.postman_environment.json" -r htmlextra

The command above will execute your collection and environment, generating a detailed HTML report. The report includes a dashboard that visually represents the results.


           
           
           
