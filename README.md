# jtwbasicexample
Project Description
This repository contains two separate Node.js applications:

Server on Port 4000

This server handles authentication using JWT (JSON Web Tokens) for generating access and refresh tokens.
It provides routes for user login (POST /login), token refresh (POST /token), and fetching posts (GET /posts).
The server utilizes environment variables for token secrets and runs on http://localhost:4000.
Client on Port 3000

This server is a basic setup to demonstrate fetching posts from the above server.
It sends a GET request to /posts with a bearer token in the authorization header to fetch posts from the authenticated server.
The server runs on http://localhost:3000.
How to Use
Setup

Clone the repository to your local machine.
Starting the Servers

Navigate to each server directory (server and client).
Run npm install to install dependencies.
Start the servers:
For Server on Port 4000: node server.js
For Client on Port 3000: node client.js
Testing with Postman

Ensure both servers are running.
Use Postman or similar tools to test the following endpoints:
POST http://localhost:4000/login with JSON body {"username": "your_username"}
POST http://localhost:4000/token with JSON body {"token": "your_refresh_token"}
GET http://localhost:3000/posts with Authorization header Bearer your_access_token
Notes

Make sure to replace your_username, your_refresh_token, and your_access_token with actual values obtained during testing.
Contributing
Feel free to fork this repository, open issues, and submit pull requests to improve the functionality or add features.
