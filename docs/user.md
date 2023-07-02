# User API Spec

## Register User API

Endpoint : POST /api/users/login

Request Body :

```json
{
    "username": "putra",
    "password": "rahasia"
}
```

Response Body Success :

```json
{
    "data": {
        "username": "putra",
        "name": "Putra Rama Setiawan"
    }
}
```

Response Body Error :

```json
{
    "errors": "username already registered"
}
```

## Login User API

Endpoint : POST /api/users

Request Body :

```json
{
    "username": "putra",
    "password": "rahasia",
    "name": "Putra Rama Setiawan"
}
```

Response Body Success :

```json
{
    "data": {
        "token": "unique-token"
    }
}
```

Response Body Error :

```json
{
    "errors": "username or password wrong"
}
```

## Update User API

Endpoint : GET /api/users/current

Headers :

-   Authorization : token

Request Body :

```json
{
    "name": "Putra Rama Setiawan", // optional
    "password": "new password" //optional
}
```

Response Body Success :

```json
{
    "data": {
        "username": "putra",
        "name": "Putra Rama Setiawan"
    }
}
```

Response Body Error :

```json
{
    "errors": "Name length max 100"
}
```

## Get User API

Endpoint : GET /api/users/current

Headers :

-   Authorization : token

Response Body Success :

```json
{
    "data": {
        "username": "putra",
        "name": "Putra Rama Setiawan"
    }
}
```

Response Body Error :

```json
{
    "errors": "Unauthorize"
}
```

## Logout User API

Endpoint : DELETE /api/users/logout

Headers :

-   Authorization : token

Response Body Success :

```json
{
    "data": "OK"
}
```

Response Body Error :

```json
{
    "errors": "Unauthorize"
}
```
