Authentication
===========

Endpoints:

- **Login**
- [login Request](#login-request)
- [login Response](#login-response)

Login Request
--------------------

* `POST /api/login` to authenticate a single user

###### Required request data 

```json
{
    "username": <String>,
    "password": <String>
}
```

###### Required request headers 
`Content-Type` should be `application/json` 

Login Response
--------------------

###### Success response Format

```json
{
    "generalStatus": <String>"success",
    "payload": <String>"Representing a JSON Web Token",
    "authStatus": <String>"yes" | "no" | "error" | "unknown"
}
```

###### Error response Format

```json
{
    "generalStatus": <String>"error",
    "payload": <String>"Contains the error message",
    "authStatus": <String>"yes" | "no" | "error" | "unknown"
}
```