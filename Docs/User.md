# User API Documentation

Base URL:
http://localhost:8080

---

## 1. Get All Users

Endpoint:
GET /api/users

Response Body (Success - 200)

```json
{
  "status": "success",
  "data": [
    {
      "id": "1",
      "name": "Kevin",
      "age": 22
    }
  ]
}
```

---

## 2. Get User By ID

Endpoint:
GET /api/users/{id}

Example:
GET /api/users/1

Response Body (Success - 200)

```json
{
  "status": "success",
  "data": {
    "id": "1",
    "name": "Kevin",
    "age": 22
  }
}
```

Response Body (Failed - 404)

```json
{
  "status": "error",
  "message": "User not found"
}
```

---

## 3. Add User

Endpoint:
POST /api/users

Request Body

```json
{
  "name": "Kevin",
  "age": 22
}
```

Response Body (Success - 200)

```json
{
  "status": "success",
  "data": {
    "id": "generated-id",
    "name": "Kevin",
    "age": 22
  }
}
```

---

## 4. Update User

Endpoint:
PUT /api/users/{id}

Example:
PUT /api/users/1

Request Body

```json
{
  "name": "Kevin Updated",
  "age": 25
}
```

Response Body (Success - 200)

```json
{
  "status": "success",
  "data": {
    "id": "1",
    "name": "Kevin Updated",
    "age": 25
  }
}
```

---

## 5. Delete User

Endpoint:
DELETE /api/users/{id}

Example:
DELETE /api/users/1

Response Body (Success - 200)

```json
{
  "status": "success delete user with id 1"
}
```