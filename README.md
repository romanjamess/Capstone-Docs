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

## GET /user

### Request:

```js
fetch(`${API}/user`);
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
        "role": "Customer",
 }
```
## GET /user

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
  ]
```

## GET /posts/:postId

### Request:

```js
fetch(`${API}/posts/280c3437-69aa-4f35-bd67-2d11b5cf0596`);
```

### Response:

```js
{
  "success": true,
  "post": {
      "id": "280c3437-69aa-4f35-bd67-2d11b5cf0596",
      "text": "how much is btc worth",
      "title": "btc",
      "userId": "b741adcd-36f2-4d83-af9b-a52f91804aa5",
      "subredditId": "88e8718f-931f-4e64-8849-67cabb6cb94a",
      "parentId": null,
      "user": {
        "id": "b741adcd-36f2-4d83-af9b-a52f91804aa5",
        "username": "katie",
        "password": "$2b$10$oFyb0maubaWpAOUZmv8HYekCILQwiMGxsRLVQl2hlzxMC3bepiDBu"
      },
      "subreddit": {
        "id": "88e8718f-931f-4e64-8849-67cabb6cb94a",
        "name": "Crypto",
        "userId": "b741adcd-36f2-4d83-af9b-a52f91804aa5"
      },
      "upvotes": [
        {
          "id": "4e6cd525-ae64-464d-9720-fa51bb7b6db4",
          "userId": "b741adcd-36f2-4d83-af9b-a52f91804aa5",
          "postId": "280c3437-69aa-4f35-bd67-2d11b5cf0596"
        }
      ],
      "downvotes": [],
      "children": [
        {
          "id": "67836f3e-0695-407e-bd0e-77d2dcb71101",
          "text": "im a child",
          "title": "child",
          "userId": "03ca1281-ddb3-4421-a8f6-22c76b6a99b8",
          "subredditId": "88e8718f-931f-4e64-8849-67cabb6cb94a",
          "parentId": "280c3437-69aa-4f35-bd67-2d11b5cf0596"
        }
      ]
    },


}
```

## POST /posts

### Request:

```js
fetch(`${API}/posts`, {
  method: "POST",
  headers: {
    "Content-Type": "application/json",
    Authorization:
      "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiIzYjExZDIzMy1mZTE0LTQ2NzgtYjAwMC03YzJkNTFkYmE3MWEiLCJpYXQiOjE2OTQ1MjE5Nzl9.6qiWcCWgOA3Wvie8pjimOs1j8irhOQy6WfdVUNhUhkU",
  },
  body: JSON.stringify({
    title: "Review of the new iphone 13 mini", // optional
    text: "it's pretty good!",
    subredditId: "f3e47327-808e-4343-b6d9-bed030c2e9ff",
    parentId: null, // optional
  }),
});
```

### Response:

```js
{
  "success": true,
  "post": {
    "id": "65ce7d00-1a16-41af-b333-58cc84d9ffd4",
    "text": "it's pretty good!",
    "title": "Review of the new iphone 13 mini",
    "userId": "03ca1281-ddb3-4421-a8f6-22c76b6a99b8",
    "subredditId": "f3e47327-808e-4343-b6d9-bed030c2e9ff",
    "parentId": null
  }
}
```

## PUT /posts/:postId

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

## DELETE /posts/:postId

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

## GET /subreddits/

### Request:

```js
fetch(`${API}/subreddits/`);
```

### Response:

```js
{
  "success": true,
  "subreddits": [
    {
      "id": "88e8718f-931f-4e64-8849-67cabb6cb94a",
      "name": "Crypto",
      "userId": "b741adcd-36f2-4d83-af9b-a52f91804aa5"
    },
    {
      "id": "9e30964a-015f-458c-842c-47382d519f13",
      "name": "Fashion",
      "userId": "b741adcd-36f2-4d83-af9b-a52f91804aa5"
    },
    {
      "id": "f3e47327-808e-4343-b6d9-bed030c2e9ff",
      "name": "Technology",
      "userId": "b741adcd-36f2-4d83-af9b-a52f91804aa5"
    }
  ]
}
```

## POST /subreddits

### Request:

```js
fetch(`${API}/subreddits`, {
  method: "POST",
  headers: {
    "Content-Type": "application/json",
    Authorization:
      "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiIzYjExZDIzMy1mZTE0LTQ2NzgtYjAwMC03YzJkNTFkYmE3MWEiLCJpYXQiOjE2OTQ1MjE5Nzl9.6qiWcCWgOA3Wvie8pjimOs1j8irhOQy6WfdVUNhUhkU",
  },
  body: JSON.stringify({
    name: "programminghumor",
  }),
});
```

### Response:

```js
{
  "success": true,
  "subreddit": {
    "id": "61980b03-2d7f-45c9-95c0-f3be8a4c6595",
    "name": "programminghumor",
    "userId": "03ca1281-ddb3-4421-a8f6-22c76b6a99b8"
  }
}
```

## DELETE /subreddits/:subredditId

### Request:

```js
fetch(`${API}/subreddits/61980b03-2d7f-45c9-95c0-f3be8a4c6595`, {
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
  "success": true,
  "subreddit": {
    "id": "61980b03-2d7f-45c9-95c0-f3be8a4c6595",
    "name": "programminghumor",
    "userId": "03ca1281-ddb3-4421-a8f6-22c76b6a99b8"
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

## POST /votes/upvotes/:postId

### Request:

```js
fetch(`${API}/votes/upvotes/0a817d6e-be92-430e-a6f4-719801738c64`, {
  method: "POST",
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
  "upvote": {
    "id": "f0e37487-4c25-475c-b8dc-6e40d8bcac6e",
    "userId": "03ca1281-ddb3-4421-a8f6-22c76b6a99b8",
    "postId": "0a817d6e-be92-430e-a6f4-719801738c64"
  }
}
```

## POST /votes/downvotes/:postId

### Request:

```js
fetch(`${API}/votes/downvotes/0a817d6e-be92-430e-a6f4-719801738c64`, {
  method: "POST",
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
  "downvote": {
    "id": "af69871c-c648-4332-8b01-fe332de2e7f4",
    "userId": "03ca1281-ddb3-4421-a8f6-22c76b6a99b8",
    "postId": "0a817d6e-be92-430e-a6f4-719801738c64"
  }
}
```

## DELETE /votes/upvotes/:postId

### Request:

```js
fetch(`${API}/votes/upvotes/0a817d6e-be92-430e-a6f4-719801738c64`, {
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
  "success": true,
  "upvote": {
    "id": "f0e37487-4c25-475c-b8dc-6e40d8bcac6e",
    "userId": "03ca1281-ddb3-4421-a8f6-22c76b6a99b8",
    "postId": "0a817d6e-be92-430e-a6f4-719801738c64"
  }
}
```

## DELETE /votes/downvotes/:postId

### Request:

```js
fetch(`${API}/votes/downvotes/0a817d6e-be92-430e-a6f4-719801738c64`, {
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
  "success": true,
  "downvote": {
    "id": "af69871c-c648-4332-8b01-fe332de2e7f4",
    "userId": "03ca1281-ddb3-4421-a8f6-22c76b6a99b8",
    "postId": "0a817d6e-be92-430e-a6f4-719801738c64"
  }
}
```
