# POS_Portal_Auth2

steps to test the api on Postman

there are two API :
1) /greeting
2) /users

follow the following step for Postman
1) put the url
  http://localhost:8080/oauth/token?password=spring&username=roy&grant_type=password&scope=read%20write&client_secret=123456&client_id=clientapp
2)choose Authorization Tab-> Type -> Basic Auth -> Username and Password
3) Then Click on Update Request button
4) then will generate code
{
    "access_token": "abe1d4a0-83d3-4817-b630-f313a48df9f2",
    "token_type": "bearer",
    "refresh_token": "7212fbeb-fd61-48aa-a42e-15fc97c6b7ea",
    "expires_in": 42793,
    "scope": "read write"
}

5)Now call the third party API like .. users
  http://localhost:8080/users

6) In hearders Part 
--> Authorization  and bearer abe1d4a0-83d3-4817-b630-f313a48df9f2 put as key and value
7) Click on the Send button
8) You will found authorized user
[
    {
        "id": 1,
        "name": "Roy",
        "login": "roy",
        "password": "spring"
    },
    {
        "id": 2,
        "name": "Craig",
        "login": "craig",
        "password": "spring"
    },
    {
        "id": 3,
        "name": "Greg",
        "login": "greg",
        "password": "spring"
    }
]
