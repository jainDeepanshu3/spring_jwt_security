# spring_jwt_security
http://localhost:8080/hello  GET Request
if you have default securty then spring will show you login page with user name and password:
username: user 
password: will be genrated on the console of your IDE copy it from there.

http://localhost:8080/hello   GET REQUEST if you implemented default security in such a manner that now user name should be foo and password would also be foo..

username: foo 
password: foo

Now if you implemented the jwt token completely then you need to send user name and password in the body part as part of POST request:
For sending request you can add postman extension to your chrome browser:
Launch it and send requried parameter as follows:

  https://localhost:8080/authenticate    POST Request as we sending object (if you set request as GET then body will not show to you as                                          an option)..
                                         Authenticate as it will process your post request and generate token for you.

  Choose radio button as raw: then only it will allow you to add the json object:
{
  "username":"foo",
  "password": "foo"
}

for above to be working set in the header part as follows:

   key: Content-Type
  value: application/json

Once you generate jwt token return as the response from the application then set header with as follows:

   key: authorization
  value: bearer token value

https://localhost:8080/hello   GET Request /hello is your Rest API which is protected by Spring security.

if you again try to handle the same API without token then access will be denied.

 With JWT token system will allow you and authorize you to access the system.

  jwt token structure: eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJmb28iLCJleHAiOjE1ODkzMDQ3NjQsImlhdCI6MTU4OTMwNDcwNH0.VzqtKmoRo-t2EOiAQUI85ghbWyFSkaqopNY59akQsH4
    

 
    
   



