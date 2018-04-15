## Create User

```bash
$ curl -s -X POST \
  ${HOST}/api/register \
  -d '{
    "email": "test03@gmail.com",
    "password": "hunter1"
  }'

{
  "active": false,
  "authorization_token": "<token>",
  "email": "two@email.com",
  "user_id": 3,
  "message": "User created successfully!",
  "name": "Nick",
  "joined": "2017-08-27T13:17:06.213240067-04:00"
}
```

## Get New Session

```bash
$ curl -s -X POST \
  ${HOST}/api/sessions/info \
  -H 'Authorization: Basic <base64Encode(email:password)>'
```

## Get Session Info

```bash
$ curl -s -X GET \
  ${HOST}/api/sessions/info \
  -H 'Authorization: Bearer <token>'

{
  "active": false,
  "email": "test02@gmail.com",
  "exp": 1503689745,
  "user_id": 4,
  "username": "test01"
}

```
