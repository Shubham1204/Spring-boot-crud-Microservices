# Spring-boot-crud

The whole back-end application divided into two microservices.
1.login_signup_microservice
  in this microservice the registration and login api present with their proper functioning.

2.get_update_details_microservice
 in this microservice getting and updating employees data api present with their proper functioning.

Api s of login_signup_microservice

1. saveEmployee

 function- save the details of employee and generate their login credentials with their phone no. And password is autogenerated.

RequestBody-{“empName”: ”String”,
                         “empContact”: ”Integer”,
                         “empEmail”: ”varChar”,
                         “empPhoto”: ”String”,
		 “skillSet”: [
                                          {“skillName”: “String”  
                                              }
                                            ]
                           }
ResponseBody-{ "code": 201,
                              "message": [ "successfully added " ], 
                              "data": {}
                            }                   
2. login

function – authenticate the credential which was enter by user and ensure that jwt is implemented for the whole authentication procedure.

RequestBody-{“contact”: “Integer”,
                         “password” : “varChar”
                       }

Api s of get_update_details_microservice

1.getEmployeeById

funtion – this api will get all the employee details whose Id  will be passed.

ResponseBody-{ "code": 200,
                              "message": [ "successfully  " ], 
                              "data": {  “empId” : “String”,
                                              “empName”: ”String”,
                                            “empContact”: ”Integer”,
                                            “empEmail”: ”varChar”,
                                            “empPhoto”: ”String”,
		                     “skillSet”: [
                                          {    “skillId” : “String”,
                                                “skillName”: “String”  
                                                      }
                                                 ]
                                               }
                                       }
                            

2. updateEmployeeById

function- this api will update the exisiting employee details by getting its empId.

RequestBody-             {      “empId” : “String”,
                                              “empName”: ”String”,
                                            “empContact”: ”Integer”,
                                            “empEmail”: ”varChar”,
                                            “empPhoto”: ”String”,
		                     “skillSet”: [
                                          {    “skillId” : “String”,
                                                “skillName”: “String”  
                                                      }
                                                 ]
                                               }
                                       }

ResponseBody-  { "code": 200,
                              "message": [ "successfully added " ], 
                              "data": {}
                            }    
Key Features to Remember:-
1. Authentication and Security should be provide by jwt.
2. Cache should be implemented either one of these ( 1.HazelCast Cache
                                                                                      2.Redis Cache)
3. Unique id should be in String format and prefix is same as entity name
     ex- Employee id be like emp0001,emp0002 .....
4. Swagger should be implemented.
5. Use Mysql for database.
6. Use gradle for project build.
7.employee photo comes in String format ex- https://whasfaljh.com



E-R Diagram 
 
