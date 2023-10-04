# Capstone-Docs

## GET /

### Request:

```js
fetch(`${API}/`);
```

### Response:

```js
{
  "success": true,
  "message": "Welcome to the Capstone Project!"
}
```

## GET /users

### Request:

```js
fetch(`${API}/users`);
```

### Response:

```js
{
  "success": true,
      "user": {
        "id": "9029ed5c-9056-4654-b568-0bf7fd92071b",
        "userId": "f42d72d4-0bb3-48b1-9ee9-4f913823a013"
        "username": "Roman",
        "password": "$2b$10$fIgbTBZV.9qY8Y65geHWMeh0hkg7gjY8uM.QVJCx5OvwZ5/C66TFi",
        "createdAt": "2023-09-30T01:38:38.435Z",
        "role": "Customer"
      }
 }
```
## GET /orders

### Request:

```js
fetch(`${API}/order`);
```

### Response:

```js
{
  "success": true,
  "orders": [
 {
  "id": "9029ed5c-9056-4654-b568-0bf7fd92071b",
  "status": "CART",
  "userId": "f42d72d4-0bb3-48b1-9ee9-4f913823a013"
 },
"user": {
         "id": "16cc9326-84e7-436b-86a3-2caa9d72ffed",
         "userId": "f42d72d4-0bb3-48b1-9ee9-4f913823a013"
         "username": "Roman",
         "password": "$2b$10$fIgbTBZV.9qY8Y65geHWMeh0hkg7gjY8uM.QVJCx5OvwZ5/C66TFi",
         "createdAt": "2023-09-30T01:38:38.435Z",
         "role": "Customer",
        },
"menuItem": [
   {	
     "id": "f629322f-0c3d-47a9-b65f-c1ffb5dc1311",
     "name": "Kelp Shake",
     "description": "A Kelp shake full of seaweed!"
   },
   {
     "id": "77efa6c6-0b96-46ac-83b6-99fe8741a6d1",
     "name": "Krabby Patty",
     "description": "Created from the gods themselves..."
   }
 ],
},
   {
    "id": "8e45d339-71e5-4e48-b08d-23b3e8b66c78",
    "status": "COMPLETE",
    "userId": "f42d72d4-0bb3-48b1-9ee9-4f913823a013"
   },
"user": {
         "id": "16cc9326-84e7-436b-86a3-2caa9d72ffed",
         "userId": "f42d72d4-0bb3-48b1-9ee9-4f913823a013"
         "username": "Roman",
         "password": "$2b$10$fIgbTBZV.9qY8Y65geHWMeh0hkg7gjY8uM.QVJCx5OvwZ5/C66TFi",
         "createdAt": "2023-09-30T01:38:38.435Z",
         "role": "Customer",
        }
"menuItem": [
   {
     "id": "f629322f-0c3d-47a9-b65f-c1ffb5dc1311",
     "name": "Kelp Shake",
     "description": "A Kelp shake full of seaweed!"
   },
   {
     "id": "77efa6c6-0b96-46ac-83b6-99fe8741a6d1",
     "name": "Krabby Patty",
     "description": "Created from the gods themselves..."
   }
  ],
 ]
}
```
## GET /menu

### Request:

```js
fetch(`${API}/menu`);
```

### Response:

```js
{
  "success": true,
  "menuItem": [
    {
      "id": "0a817d6e-be92-430e-a6f4-719801738c64",
      "name": "Krabby Patty",
      "category": Burgers,
    }
    {		
      "id": "df7595d1-bacf-4656-81b7-d989beff0d86",
      "name": "Kelp Shake",
      "category": Drinks,
    }
   ]
 }
```

## GET /menuItem/:menuItemId

### Request:

```js
fetch(`${API}/menuItem/280c3437-69aa-4f35-bd67-2d11b5cf0596`);
```

### Response:

```js
{ 
"success": "true",
"menuItem": 
   {
     "id": "f629322f-0c3d-47a9-b65f-c1ffb5dc1311",
     "name": "Kelp Shake",
     "description": "A Kelp shake full of seaweed!"
   }
}
```


## PUT /order/orderId

### Request:

```js
fetch(`${API}/posts/28006818-1695-4984-83e9-bf0e6a864e08`, {
  method: "PUT",
  headers: {
    "Content-Type": "application/json",
    Authorization:
      "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiIzYjExZDIzMy1mZTE0LTQ2NzgtYjAwMC03YzJkNTFkYmE3MWEiLCJpYXQiOjE2OTQ1MjE5Nzl9.6qiWcCWgOA3Wvie8pjimOs1j8irhOQy6WfdVUNhUhkU",
  },
  body: JSON.stringify({
    title: "Review of the new iphone 13 mini - Updated!", // optional
    text: "it's not actually that good!", // optional
  }),
});
```

### Response:

```js
{
  "success": true,
  "post": {
    "id": "65ce7d00-1a16-41af-b333-58cc84d9ffd4",
    "text": "it's not actually that good!",
    "title": "Review of the new iphone 13 mini - Updated!",
    "userId": "03ca1281-ddb3-4421-a8f6-22c76b6a99b8",
    "subredditId": "f3e47327-808e-4343-b6d9-bed030c2e9ff",
    "parentId": null
  }
}
```

## DELETE /users/:userId

### Request:

```js
fetch(`${API}/posts/65ce7d00-1a16-41af-b333-58cc84d9ffd4`, {
  method: "DELETE",
  headers: {
    Authorization:
      "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiIwM2NhMTI4MS1kZGIzLTQ0MjEtYThmNi0yMmM3NmI2YTk5YjgiLCJpYXQiOjE2OTQ0MzUxNzJ9.AbFuHRnxTB1Ztgcf2S4nwn2NjuvGmV96iUx3TJN5zFk",
  },
});
```

### Response:

```js
{
  "success": true,
      "user": {
        "id": "9029ed5c-9056-4654-b568-0bf7fd92071b",
        "userId": "f42d72d4-0bb3-48b1-9ee9-4f913823a013"
        "username": "Roman"
     }
 }
```


## POST /users/register

### Request:

```js
fetch(`${API}/users/register`, {
  method: "POST",
  headers: {
    "Content-Type": "application/json",
  },
  body: JSON.stringify({
    username: "max2",
    password: "123",
  }),
});
```

### Response:

```js
{
  "success": true,
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI2MDY1MjQ3Ny0yZDY1LTQzYzctYTJmMS1mMzU4ZTQyMGQxYWEiLCJpYXQiOjE2OTQ1Mjk3MDh9.a1HjJulV55JAwyKfKt8sTjpq0AKgGcahBNM1efgFE5g"
}
```

## POST /users/login

### Request:

```js
fetch(`${API}/users/login`, {
  method: "POST",
  headers: {
    "Content-Type": "application/json",
  },
  body: JSON.stringify({
    username: "max2",
    password: "123",
  }),
});
```

### Response:

```js
{
  "success": true,
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI2MDY1MjQ3Ny0yZDY1LTQzYzctYTJmMS1mMzU4ZTQyMGQxYWEiLCJpYXQiOjE2OTQ1Mjk3MDh9.a1HjJulV55JAwyKfKt8sTjpq0AKgGcahBNM1efgFE5g"
}
```

## GET /users/token

### Request:

```js
fetch(`${API}/users/token`, {
  headers: {
    Authorization:
      "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiIzYjExZDIzMy1mZTE0LTQ2NzgtYjAwMC03YzJkNTFkYmE3MWEiLCJpYXQiOjE2OTQ1MjE5Nzl9.6qiWcCWgOA3Wvie8pjimOs1j8irhOQy6WfdVUNhUhkU",
  },
});
```

### Response:

```js
{
  "success": true,
  "user": {
    "id": "03ca1281-ddb3-4421-a8f6-22c76b6a99b8",
    "username": "max"
  }
}
```



## DELETE /order/menuitem/:menuitemId

### Request:

```js
fetch(`${API}/order/menuitem/0a817d6e-be92-430e-a6f4-719801738c64`, {
  method: "DELETE",
  headers: {
    Authorization:
      "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiIzYjExZDIzMy1mZTE0LTQ2NzgtYjAwMC03YzJkNTFkYmE3MWEiLCJpYXQiOjE2OTQ1MjE5Nzl9.6qiWcCWgOA3Wvie8pjimOs1j8irhOQy6WfdVUNhUhkU",
  },
});
```

### Response:

```js
{ 
"success": "true",
"menuItem": 
   {
     "id": "f629322f-0c3d-47a9-b65f-c1ffb5dc1311",
     "name": "Kelp Shake",
     "description": "A Kelp shake full of seaweed!"
   }
}
```



