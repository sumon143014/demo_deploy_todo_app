# demo_deploy_todo_app

api descriptions:

1. LOGIN [POST]: `/api/login`
  required login data:
  these must be included in `request body`
  example:
      ```
      {
      "email": "youremail@domain.com",
      "password":"complexPasswords"
      }
      ```
   after successfull login [not by using previous `token`]  you'll get a new token back.
   
   => LOGIN  usign Authorization token: 
      add `Authorization` token in your header or `x-access-token` you may preceed the token with `Bearer`

2. REGISTER [POST]: `/api/register/`
  required register data:
  these must be included in `request body`
  example:
      ```
      {
      "name": "Full Name",
      "email": "youremail@domain.com",
      "password":"complexPasswords"
      }
      ```
   
   => REGISTER using `Authorization`
      add `Authorization` token in your header or `x-access-token` you may preceed the token with `Bearer`
3. LGOUT [POST]: `/api/logout` [need to be authenticated first] 
      to end all active `sessions` add these to the `body` of your `POST request`
      ```
      "endAllSession" : true
      ```
