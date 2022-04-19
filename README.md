# UserLogin
JWT Authentication And Authorization In .NET 6.0 With Identity Framework


We must install the 4 libraries below into the new project. 

Microsoft.EntityFrameworkCore.SqlServer 
Microsoft.EntityFrameworkCore.Tools 
Microsoft.AspNetCore.Identity.EntityFrameworkCore 
Microsoft.AspNetCore.Authentication.JwtBearer 


----------------------------------------------------------------------------------------------------------------------------------

We must create a database and tables needed before running the application. As we are using entity framework, we can use below database migration command with package manger console to create a migration script. 
“add-migration Initial” 
Use the command below to create database and tables. 
“update-database” 

----------------------------------------------------------------------------------------------------------------------------------
Login (Get Token)
            curl -X 'POST' \
              'http://localhost:5011/api/Authenticate/login' \
              -H 'accept: */*' \
              -H 'Content-Type: application/json' \
              -d '{
              "username": "Bekirhan",
              "password": "xxxXXxxX"
            }'

Register 
            curl -X 'POST' \
              'http://localhost:5011/api/Authenticate/register' \
              -H 'accept: */*' \
              -H 'Content-Type: application/json' \
              -d '{
              "username": "Bekirhan",
              "email": "bekirhangultoplayan@gmail.com",
              "password": "xxxXXxxX"
            }'

