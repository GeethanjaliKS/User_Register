# User_Register
# User Register Backend using Node.js and Prisma
This is a backend application built with Node.js and Prisma ORM that handles user registration and stores user data in a database. The application provides endpoints to create, retrieve, update, and delete user records.

## Getting Started
To use this application, you need to have Node.js and npm (Node Package Manager) installed on your system. Additionally, you will need to set up a PostgreSQL database where user data will be stored.

## Installation
npm init -y ===>Install the node js
"Run npm i in the terminal to install all the packages as already listed in the dependencies section of the package.json file."
"dependencies": {
    "cors": "^2.8.5",
    "express": "^4.18.2",
    "pg": "^8.11.2",
    "prisma": "^5.1.1"
  },
  "devDependencies": {
    "@prisma/client": "^5.1.1",
    "nodemon": "^3.0.1"
  }
  ## Schema
  model User {
  id       Int      @id @default(autoincrement())
  username String
  email    String   @unique
  age      Int?
}
## Run the program
When there are any changes in the schema, you can run the following commands in the terminal:
To create and apply a new migration for the changes:
npx prisma migrate dev --name init
To generate the Prisma Client based on the updated schema:
npx prisma generate
To run the server:
nodemon Server.js



  

  

  
