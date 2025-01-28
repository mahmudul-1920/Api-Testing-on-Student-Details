### **Student API Testing with Postman Newman**
This project demonstrates API testing using Postman, providing a collection of tests to validate various endpoints of the API. 

### **Features**

- Tests for GET, POST, PUT, DELETE requests
- Collection of tests covering different API endpoints
- Environment setup for easy switching between environments
- Pre-request scripts for data setup
- Test scripts for assertions and validations

## API Documentation:
- https://docs.google.com/document/d/1LF3FeN4obAZTn-QeuWZzteLn8X1m8ww2/edit
  
### **Technology used:**
- Postman
- Newman

### **Prerequisite:**
- Node Js
- Newman
- Newman Html Report Library

### **Installation**

1. Postman: If you haven't already, [download and install Postman.](https://www.postman.com/downloads/)
2. Clone the repository:
 ```console 
  git clone https://github.com/mahmudul-1920/Api-Testing-on-Student-Details.git
```
3. Import the Postman collection:
    - Open Postman.
    - Click on the Import button.
    - Select the file from the repository.
4. Import the Postman environment:
    - In Postman, click on the gear icon in the top right corner.
    - Select **Import** and choose the file.
5. Newman and Report Installation Process:
    - Newman Install Command:
     ```console 
      npm install -g newman
    ```
    - Newman Html Report Install Command:
     ```console 
      npm install -g newman-reporter-htmlextra
    ```
### **Usage**
1. Select Environment:
    -   In Postman, select the appropriate environment (e.g., Development, Production) from the top-right dropdown.
3. Run Collection:
    -   Select the imported collection from the Collections sidebar.
    -   Click on the Runner button to open the collection runner.
    -   Select the desired environment.
    -   Click Start Test to run the collection.
8. View Results:
    -   Once the tests are complete, view the results in the Runner tab.
    -   Detailed test results can be viewed for each request.

## **Testing**

## Test Case Scenarios:

 ## _**1. Get Student Details **_
### Request URL: https://thetestingworldapi.com/api/studentsDetails
### Request Method: GET
### Response Body:

    [
    {
        "id": 526717,
        "first_name": "Anna",
        "middle_name": "Banana last_name=Uzumaki",
        "last_name": null,
        "date_of_birth": "12/23/1990"
    },
    {
        "id": 526716,
        "first_name": "sample ",
        "middle_name": "sample ",
        "last_name": "sample ",
        "date_of_birth": "sample "
    },
    {
        "id": 526715,
        "first_name": "Anna",
        "middle_name": "Banana last_name=Uzumaki",
        "last_name": null,
        "date_of_birth": "12/23/1990"
    }
    ]


## _**2. Create Student **_

### Request URL: https://thetestingworldapi.com/api/studentsDetails
### Request Method: POST
### Pre-request Script:
```console 
{
  "first_name": "sample string 2",
  "middle_name": "sample string 3",
  "last_name": "sample string 4",
  "date_of_birth": "sample string 5"
}


Response: {
    "id": 526718,
    "first_name": "sample string 2",
    "middle_name": "sample string 3",
    "last_name": "sample string 4",
    "date_of_birth": "sample string 5"
}



```
 ## _**3. Get Student Details by id **_
### Request URL: https://thetestingworldapi.com/api/studentsDetails/{{id}}
### Request Method: GET
### Response Body:
 ```console 
{
    "status": "true",
    "data": {
        "id": 526716,
        "first_name": "sample ",
        "middle_name": "sample ",
        "last_name": "sample ",
        "date_of_birth": "sample "
    }
}

```

## Run Command:  
- Run Command for Console: 
```console 
newman run Student.postman_collection.json -e Students_Environment.postman_environment.json  
```
- Run Command for Report: 
```console 
newman run Student.postman_collection.json -e Students_Environment.postman_environment.json -r cli,htmlextra
```

## Newman Report Summary:
![Newman Report Summary](https://github.com/mahmudul-1920/Api-Testing-on-Student-Details/blob/69dedecb84dc7ac5ac6231214b841b75a4b68f42/student%20report%20summary.png)
![Newman Report Summary](https://github.com/mahmudul-1920/Api-Testing-on-Student-Details/blob/b74ab96ca73c2d6dd4555971fb579d58a53be6cf/student%20report%20summary2.png)
![image](https://github.com/mahmudul-1920/Api-Testing-on-Student-Details/blob/a867f98ba9f7c17aa2a3c0e23fc3b7dbbf5b41dd/Screenshot_23.png)
![Newman Report Summary](https://github.com/mahmudul-1920/Api-Testing-on-Student-Details/blob/c4a2b30577d0b406b0861656cb6b1409708d6fcd/Screenshot_24.png)
