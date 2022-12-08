# DOCUMENTATION

## ABOUT
The product API was created because it was my teaching material to create an API using the Kotlin programming language. This project was created using the spring framework with a spring initializer to generate the project and uses several dependencies to support this project so that it can run.

This repo is also expected to be good documentation and teaching material for me or visitors who want to know how code is made to create APIs using the Kotlin programming language and at the same time serve as documentation for me in the future.

## START PROJECT

If you want to build by your own please follow the steps below :
  - We will using Spring Framework
  - For setting up the project, you can use Spring Starter
    - Open browser, and find <a href="https://start.spring.io">Spring Initializer</a>, to generate project not manually in our IDE but onlinely.
    - Choose Gradle-Kotlin because mostly kotlin users are using grade to manage the packages or depencies.
    - Choose Kotlin language because we will develop our API using that language
    - Choose depedencies needed in our project
      1. Web Spring
      2. Spring Data JPA
      3. MySQL Driver
    - Finally, click generate to create your project
  - After the folder downloaded, extract it and open in your IDE or text editor. Recommended if you use <a href="https://www.jetbrains.com/idea/download/#section=mac">IntellijIDEA.in</a> because I personally feel so easily to write my code and the debugger is so informative for me to fix our error.
  - You can check your build.gradle.kts for checking our depedencies which is downloaded before when generate our project
  - Then, you can start to writing codes to create API
  - Or, you can download or clone this repo to see how my code works

## API ENDPOINT

### Get Product

Request :

- Method : GET
- Endpoint : `/api/products`
- Header :
  - Accept: application/json

Response :

```json
{
  "code": "integer",
  "status": "string",
  "data": [
    {
      "id" : "long, unique",
      "name" : "string",
      "price" : "long",
      "quantity" : "integer",
      "createdAt" : "date",
      "updatedAt" : "date"
    },
  ]
}
```

### List Product

Request :

- Method : GET
- Endpoint : `/api/products`
- Header :
  - Accept: application/json
- Query Param :
  - size : number
  - page : number

Response :

```json
{
  "code": "integer",
  "status": "string",
  "data": [
    {
      "id" : "long, unique",
      "name" : "string",
      "price" : "long",
      "quantity" : "integer",
      "createdAt" : "date",
      "updatedAt" : "date"
    },
    {
      "id" : "long, unique",
      "name" : "string",
      "price" : "long",
      "quantity" : "integer",
      "createdAt" : "date",
      "updatedAt" : "date"
    },
  ]
}
```

### Post Product

Request :

- Method : POST
- Endpoint : `/api/products`
- Header :
  - Content-Type: application/json
  - Accept: application/json
- Body :

```json
{
    "id" : "long, unique",
    "name" : "string",
    "price" : "long",
    "quantity" : "integer",
}
```

Response :

```json
{
  "code": "integer",
  "status": "string",
  "data": [
    {
      "id" : "long, unique",
      "name" : "string",
      "price" : "long",
      "quantity" : "integer",
      "createdAt" : "date",
      "updatedAt" : "date"
    },
  ]
}
```

### Update Product

Request :

- Method : PUT
- Endpoint : `/api/products/{id}`
- Header :
  - Content-Type: application/json
  - Accept: application/json
- Body :

```json
{
    "name" : "string",
    "price" : "long",
    "quantity" : "integer",
}
```

Response :

```json
{
  "code": "integer",
  "status": "string",
  "data": [
    {
      "id" : "long, unique",
      "name" : "string",
      "price" : "long",
      "quantity" : "integer",
      "createdAt" : "date",
      "updatedAt" : "date"
    },
  ]
}
```

### Delete Product

Request :

- Method : DELETE
- Endpoint : `/api/products/{id}`
- Header :
  - Accept: application/json

Response :

```json

```

