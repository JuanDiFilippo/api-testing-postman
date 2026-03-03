# API-testing-postman

## Project Overview

This project contains a Postman collection designed to validate the structure and behavior of publicly available REST APIs.  
The goal is to demonstrate fundamental API testing practices using automated test scripts within Postman.

## APIs Tested

The following endpoints from JSONPlaceholder were used:

- https://jsonplaceholder.typicode.com/users
- https://jsonplaceholder.typicode.com/comments
- https://jsonplaceholder.typicode.com/photos

## Validations Implemented

For each endpoint, the following validations are performed:

- HTTP status code verification (200 OK)
- JSON response parsing
- Validation of required properties
- Data type assertions (string, number)
- Nested object validation (e.g., address.city)
- Response time threshold checks

## Example Validation Logic

Tests include:

- Ensuring each object in the response array contains required fields
- Verifying nested properties exist within parent objects
- Asserting correct data types for key fields
- Validating response time against defined performance limits

## How to Run

1. Open Postman
2. Import the `API_Test.postman_collection.json` file
3. Run the collection using the Collection Runner
4. Review test results in the Postman console

---

This project demonstrates practical API testing fundamentals and structured validation of REST responses using Postman.
