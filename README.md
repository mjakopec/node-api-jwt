# node-api-jwt
Create Simple API with jsonwebtoken protection
You need MongoDB server already installed

Create .env file in root with:

MONGO_URI = "mongodb://localhost/node-api"

PORT = 8050

TOKEN_KEY=XXXX-FIND SOME TOOL OR SCRIPT TO GENERATE BIG TOKEN KEY-XXXX

1. npm init
2. npm install dotenv express bcryptjs jsonwebtoken mongoose
3. node server.js

Test app in Postman
To register user use:
  POST http://localhost:8050/register
  body {
  "first_name":"John",
  "last_name":"Doe",
  "email":"JD@example.com",
  "password": "xxx"
  }
 
 To login use:
  POST http://localhost:8050/login
  body {
  "email":"JD@example.com",
  "password": "xxx"
  }
  when you get token ey... use it for get data
  GET http://localhost:8050/welcome
  body {
  "token":"ey...."
  }
  
  OR You can use:
  http://localhost:8050/welcome?token=ey....
  (but then without token in body)
