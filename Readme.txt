Postman Project description:

The collection named "Task" consist of 2 folders:

*The first folder executed in the following steps to verify Testcases (valid login credentials, invalid login credentials):

after getting login link: Get method: https://pay2.foodics.dev/cp_internal/login 

1)Enter with Valid Credentials: Post with valid credentials, expected: response status 200 Ok should be displayed and the response body display (Access token) or return content of page in response body and status 200 ok displayed, actually it display content of page in response body with status OK. (test case status : Pass, (according to what expected in API documentation))

2)Enter with inValid Password: Post with invalid Password, response status should be "400 Bad Request" and display in response body ("Invalid Credentials"), while actually it display content of the page in the response body with "status 200 Ok" (Test case status: failed)

3)Enter with inValid merchant email: Post with invalid Email, response status should be "400 Bad Request" and display in response body ("Invalid Credentials"), while actually it display content of the page in the response body with "status 200 Ok" (Test case status: failed)

*The second folder executed to test Page Who am I:(Test case: not to proceed to this page when invalid login credentials posted at login URI)

after getting login link: Get method: https://pay2.foodics.dev/cp_internal/login 

1)Enter with InValid Credentials/WhoamI: Post with invalid credentials, response status should be "400 Bad Request" and display in response body ("Invalid Credentials"), while actually it return status 200 OK .

2)Moving to Page WhoamI with invalid credentials: When Getting uri: https://pay2.foodics.dev/cp_internal/whoami, invalid message "cannot move to WhoamI page, unauthorized" 
should be displayed in response body, while actually the admin page normally displayed in the response body with status 200 OK. (Test case status: failed)

