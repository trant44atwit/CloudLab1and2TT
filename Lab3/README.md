# Lab 3 Node.js Express Web Service

## Introduction

This project is a simple Node.js web service using **Express**. It includes a variety of routes that return HTML Content, have query parameters, header parameters, and body inputs.

---

## Description

This Express app features:

- **5 HTML routes** (return plain text content)
- **5 routes with query parameters** (perform simple logic based on query inputs)
- **1 route that uses a custom header**
- **1 route that accepts JSON body input via POST**

It serves as an example of handling different types of requests in the Node.js service.

---

## Design

### Packages
- Node.js
- Express.js

### Route Overview

| Route (Examples)         | Method | Type              | Description                                 |
|--------------------------|--------|-------------------|---------------------------------------------|
| `/`                      | GET    | HTML              | Returns "Hello World!"                      |
| `/hello_there`           | GET    | HTML              | Returns a Star Wars meme reference          |
| `/contact`               | GET    | HTML              | Returns email contact info                  |
| `/crazy`                 | GET    | HTML              | Returns a quote                             |
| `/about`                 | GET    | HTML              | Returns a vague message                     |
| `/search?q=word`         | GET    | Query             | Echoes back the search term                 |
| `/heyo?name=Timmy`       | GET    | Query             | Personalized greeting using name            |
| `/sum?a=3&b=4`           | GET    | Query             | Returns the sum of two integers             |
| `/subtract?a=10&b=4`     | GET    | Query             | Returns the difference of two integers      |
| `/multiply?a=3&b=5`      | GET    | Query             | Returns the product of two integers         |
| `/header`                | GET    | Header            | Reads a `token` from the request header     |
| `/submit`                | POST   | JSON Body         | Accepts and returns a name and age JSON     |
Note: For the queries, the string or integer after the "=" can be replaced with your own.
---

## How to Run the Project (In VS Code)

### Install Dependencies

Make sure Node.js is installed. Then run these commands in the terminal of the directory for Lab 3 if package.json and package-lock.json are not present:

"npm init -y"

"npm install express"

### Running the server

After, type in the terminal "node server.js" then click on the provided web link (http://localhost:8080/).

To test routes, type in the routes shown above. Try your own parameters too!

**Note:** For header and submit, use Postman to test the token for /header and POST for /submit. Make sure the service is running!

On the homepage of Postman, click "New Request".

### Header Testing

Make sure the request is "GET".

Type into the URL section: http://localhost:8080/header

Navigate to the Headers Tab and under "Key", type in "Token" then a value next to it.

Hit "Send" and the terminal in Postman will display the Key and Value.

### Submit Testing

Make sure the request is "POST".

Type into the URL section: http://localhost:8080/submit

Navigate to the Body tab and click on "raw"

Copy and paste this into the body:

{
  "name": "",
  "age": 
}

Fill in your own parameters then click "Send".

The terminal in Postman will display the name and age just inputted.
