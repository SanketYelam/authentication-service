For Login Service:
Rule: Validate User
Description: This rule validates a user based on the provided username and password.
Conditions:
When a LoginRequest object is received with a non-null username and password.
There exists a Users object in the system with the same username and password.
Actions:
If the conditions are met, a LoginResponse object is created with a status of "Success" and a message indicating successful login.
The response object is modified and set in the LoginRequest object.
Rule: Invalid User
Description: This rule handles the case when a user with the provided username and password does not exist.
Conditions:
When a LoginRequest object is received.
There does not exist any Users object in the system with the same username and password as in the request.
Actions:
If the conditions are met, a LoginResponse object is created with a status of "Fail" and a message indicating failed login.
The response object is modified and set in the LoginRequest object.
