# User_Register
# User Register Backend using Node.js and Prisma
This is a backend application built with Node.js and Prisma ORM that handles user registration and stores user data in a database. The application provides endpoints to create, retrieve, update, and delete user records.

## Getting Started
To use this application, you need to have Node.js and npm (Node Package Manager) installed on your system. Additionally, you will need to set up a PostgreSQL database where user data will be stored.
Install PostgreSQL in your browser and provide a password. Ensure that the password for the database URL is the same, and then create the database. If you change the password, make sure to update it on both sides.

## Installation
npm init -y ===>Install the node js
"Run npm i in the terminal to install all the packages as already listed in the dependencies section of the package.json file."

  ## Schema
model User {
  id         Int      @id @default(autoincrement())
  username   String
  email      String   @unique
  age        Int?
  fullname   String
  gender     String
  password   String
}

## Run the program
When there are any changes in the schema, you can run the following commands in the terminal:
To create and apply a new migration for the changes:
npx prisma migrate dev --name init
To generate the Prisma Client based on the updated schema:
npx prisma generate
To run the server:
nodemon Server.js



  

  

  
