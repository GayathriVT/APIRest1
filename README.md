# Petstore API automation 

## Framework Overview

The API test framework is developed in RestAssured - TestNG - maven framework

### Test Scenarios:

Create the following automated API tests for DEMO PET STORE https://petstore.swagger.io/ :

1. Get Request for reading all available pets. Assert expected result for "available" status
2. Post a new available pet to the store. Assert new pet added.
3. Get request to find the pet by id. Assert expected result for Id and name
4. Update this pet status to "sold". Assert status updated.
5. Delete this pet. Assert deletion.
6. Delete request to delete already deleted pet, operation fails with Error code 404.Assert expected result - Negative TC. 
7. Get request to find pet by the deleted id - already deleted pet should not exist.Assert expected result for message - Negative TC

### Run

Test execution : the tests were executed from IntelliJ
To run the TestNG tests use the command: mvn clean test
To generate allure report use the command: allure serve allure-results
To view the report, use the following command: allure open allure-report

Folder Structure src/test/java: src/test/resources: FileReader for PetToUpload.json
Testng File is "testngPetStore.xml"
 

## Areas of improvement: 
Handle payload data - Implementation of data serialisation using Jackson api

## Test Results

![image](https://github.com/user-attachments/assets/a8a116b4-3cf8-42c7-9728-8ffb25df5af2)

![image](https://github.com/user-attachments/assets/63668060-ecb0-4390-a9f4-ecfec0c5530c)



