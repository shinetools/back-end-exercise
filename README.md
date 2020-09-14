# Back-end exercise

The goal of this exercise is to see if you're confortable with JavaScript and/or TypeScript and are used to writing functional, well **tested** and **documented** API endpoints.

We'll be working on a micro service, called `users-service`, which is responsible for all CRUD operations on the `Users` table in the `Exercise` database. We'll use sqlite in this exercise as it requires no setup.

The exercise is divided in steps. Each step will be reviewed independently using pull requests.

## Setup

1. Fork the repo
2. Clone the repo on your computer
3. Install the dependencies

## Description

1. Create the Users table

```
Users
- userId PRIMARY KEY
- firstName
- lastName
- fullName
- email
- birthdate
- street
- city
- country
- zip
- status ENUM (ACTIVE/LOCKED/CLOSED)
- createdAt
- updatedAt
```

2. Write the CRUD endpoints
3. Add an authentication layer using JWT. We'll assume that an another service is responsible for generating valid JWTs.
4. Write a script to insert a bunch of test data
5. Add a second table named UserSettings following the following schema:

```
UserSettings
- userSettingId PRIMARY KEY
- userId FOREIGN KEY
- hasSubscribedToNewsletter
- defaultCurrency
```

6. Write the CRUD endpoints for this new table
7. Allow the user's GET endpoint to return the userSettings alongside the user object

## Requisites

- All endpoints must be tested
- All endpoints must be documented
- All endpoints should validate their inputs
