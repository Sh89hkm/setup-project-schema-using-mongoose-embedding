# Setup project schema using Mongoose with embedding

## Objectives

- Practice setting up MongoDB collection schemas and models using mongoose
- Practice relating documents to each other using embedding method

## Overview

We have learnt a little bit about building schemas using MongoDB and mongoose, and the difference between embedding documents and referencing documents. In this assignment, we are going to build the schema using Mongoose for a blog website which has blog posts and authors and we will be embedding one of the document in the other.

## Starter Code

You will find the following starter code in the project folder:

- Basic Express application setup in `index.js`
- Database connection setup in `db/connection.js`

All the necessary packages are already listed in `package.json`.

## Instructions

Create a `models` folder in the project and write a model for embedded BlogPost and Author schema. Your code must include:

- the base structure of each document using mongoose built-in methods for schemas
- Embed one of the documents in the other the way you feel makes more sense.

### Part 0: Building the embedded schema

We will have just one collection. This could be blogPosts having author embedded inside each document, or authors having blogPosts embedded. Which approach do you think is better?

Whichever approach you choose, make sure blogPost has the following fields:

- Title as a string
- Content as a string
- Array of tags where each tag is a string

And author has the following fields:

- Name as string
- Age as number
- Gender as string
- Nationality as string
- Array for areas of expertise where each is a string

**Hint**: Google and documentation!

## Working with docker

This app is bootstraped with docker and docker-compose. It containerize the server, as well as the database.

### To start the server

run the command `yarn && yarn start`. This will install all the dependencies and build the docker image

### To install packages

when you run `yarn add PACKAGE` the package will be installed in docker as well automatically. However if you run into issues, you need to stop the server first with `yarn run stop` then you can run `yarn run build` to rebuild the docker image and start again.

### To prune the containers and data

> ⚠️ WARNING: This is a destructuve command that would delete the containers and all the data inside like database data, and uploads

you can run `yarn run prune` to shutdown the server and delete all the volumes associated with it. This serves as a start fresh command, that will return your server environment to original. It will not affect your code changes though.

## Submission

You can manually test your models by creating a few API endpoints on the `index.js` file for adding and finding authors and blogposts. Then call these endpoints to test your models. You can also verify the database operations by checking the collections using any MongoDB GUI tool or Mongo shell.

Once you're ready to submit the assignment, follow these steps on your terminal:

1. Stage your changes to be committed: `git add .`
2. Commit your final changes: `git commit -m "solve assignment"`
3. Push your commit to the main branch of your assignment repo: `git push origin main`

After your changes are pushed, return to this assignment on Canvas for the final step of submission.
