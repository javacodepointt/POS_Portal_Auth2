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


# Step 1:
![step1](https://user-images.githubusercontent.com/29585710/38096494-9cdfc79a-3390-11e8-81c8-6e15f24e9996.PNG)

# Step 2:
![step2](https://user-images.githubusercontent.com/29585710/38096698-26c20068-3391-11e8-9dda-766ee0101bb3.png)

# Step 3:
![step3](https://user-images.githubusercontent.com/29585710/38096717-3458c3f6-3391-11e8-83a5-d45fa41a30ab.png)

# Step 4:
![step5](https://user-images.githubusercontent.com/29585710/38096735-3b98852a-3391-11e8-904d-e52d66416860.png)

# Step 5:
![step6](https://user-images.githubusercontent.com/29585710/38096733-3b3944ca-3391-11e8-8cc3-008aa196813c.png)


