Frmework Overview 

The API test framework is developed in RestAssured - TestNG - maven framework
Setup:
1. Clone the repository:
2. 



Allure Report

Folder Structure
src/test/java: 
src/test/resources: FileReader for payload

petstore-rest-assured
The testing framework for PetStore-service: https://petstore.swagger.io/
Get "available" pets. Assert expected result
Post a new available pet to the store. Assert new pet added.
Update this pet status to "sold". Assert status updated.
Delete this pet. Assert deletion.

Run

For run tests use the command:
mvn clean test

For generate allure report use the command:
allure serve allure-results

To view the report, use the following command:
allure open allure-report

Execute your TestNG tests using Maven:
mvn clean test

Test execution : the tests were executed from IntelliJ
the code does some additional testing, such as "trying to delete already deleted pet", "trying to get not existing pet (because it was deleted)
   
   - the test execution order is controlled by priority as parameter of @Test annotations. If priority is not set, then some tests may fail, as the test may try to 
     delete a Pet, that was not uploaded (operation POST must preceed DELETE), etc.

     ![image](https://github.com/user-attachments/assets/2d7d1d8d-4fbb-48eb-a172-3c47818e5d57)

