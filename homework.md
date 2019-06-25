# Homework: Full Stack Games Hub App

### Learning Objectives

- Understand the relationship between client, server and database
- Be able to navigate a codebase that you haven't written

## Brief

Your boss has asked to you look over the codebase of a full-stack JavaScript application. The front-end is written in JavaScript using Vue, the back-end uses an Express server and a MongoDB database. Your task is to make yourself familiar with the codebase.


## MVP

### Task

Draw a diagram showing the dataflow through the application starting with a form submission, ending with the re-rendering of the page. This will involve a multi-direction data-flow with the client posting data to the server and the server sending data back to the client with the response. Detail the client, server and database in the diagram and include the names of the files involved in the process.

### Questions

1. What is responsible for defining the routes of the `games` resource?
*The router in 'server/helpers/create_router.js defines the routes for 'games', which is called in server.js.*

2. What do you notice about the folder structure?  Whats the client responsible for? Whats the server responsible for?
*The app is separated cleanly into two parts. The client is the front end which is user interacts with, and the server is the backend which handles the database and routing.*

3. What are the the responsibilities of server.js?
*server.js is responsible for accessing the database and creating routes for the app.*

4. What are the responsibilities of the `gamesRouter`?
*gamesRouter handles and API requests sent to '/api/games'*

5. What process does the the client (front-end) use to communicate with the server?
*The client uses Fetch requests to access the server via API requests.*

6. What optional second argument does the `fetch` method take? And what is it used for in this application?
*The second argument is an init object that allows you to control a number of different settings. In this app it defines the method used, converts our payload to JSON, and attaches headers.*

7. Which of the games API routes does the front-end application consume (i.e. make requests to)?
*Our app uses, POST, GET and DETELE requests.*

8. What are we using the MongoDB Driver for?
*The driver allows us to interact with MongoDB using JavaScript, in particular callbacks and promises for our API requests.*

## Extension

Why do we need to use `ObjectId` from the MongoDB driver?
*We need to use `ObjectId` as it allows us to take a sting and convert it to an ID object for requesting results from the database.*

Add to your diagram the dataflow for removing a game.
