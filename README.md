API Testing with Postman




Postman is an application used for API testing
POSTMAN Request





There are mainly several types of postman request. But in here we are going to talk about some five kinds of request.
•	Post- New input request to the server.
•	Put - Value Update request to the server.
•	patch- One section modify request to server.
•	Get- value generate request from server.



Environment Setup
For set up an environment . You have to create a new environment and rename the environment. And you have to put some JS Script on the such environment. As like for id set up in environment
var jsonData = pm.response.json();
pm.environment.set("id", jsonData.bookingid)
Permission Set Up
Why do we need permission in PostMan. We need permission to update/patch/delete values in API.
For permission , the developer will give you permission like {“Admin:admin” “Password:Password1234”}
Now open permission request with Get request and test script will be
var jsonData=pm.response.json(); pm.environment.set("access", jsonData.token) you will find token on the body. And set this token to environment.
Querry Parameters.



Query parameters are some additional data that we can submit with our request through API. Query parameters are optional.
Newman
1.	Go to the folder where you export collection and environment
2.	Click on folder location bar and type CMD
3.	In CMD type: Newman run (collection name) -e (environment name) -r cli,htmlextra

