# README.md for Real-Time Chat Application
=====================================================

## Overview
This is a real-time chat application built using Node.js, Express, and Socket.IO. The application allows users to join chat rooms and communicate with each other in real-time.

## Features
* Real-time messaging: Users can send and receive messages in real-time.
* Chat rooms: Users can join and leave chat rooms.
* User list: Users can see a list of all users in the chat room.
* Room list: Users can see a list of all active chat rooms.
* Activity updates: Users can see when other users are typing or active in the chat room.

## Server-Side Code
### server.mjs
The server-side code is written in JavaScript and uses the following dependencies:

* `express`: A popular Node.js web framework.
* `socket.io`: A library for real-time communication.

## Server Configuration
### Port
The server listens on port 3500 by default, but can be configured to listen on a different port using the `PORT` environment variable.

### CORS
The server allows CORS requests from `http://localhost:5500` and `http://127.0.0.1:5500` by default, but can be configured to allow requests from other origins using the `NODE_ENV` environment variable.

## Client-Side Code
The client-side code is not included in this repository, but it is assumed to be a web application that connects to the server using Socket.IO.

## API Endpoints
### /
The root endpoint that serves the chat application.

### /room
The endpoint that handles room-related events, such as joining and leaving rooms.

### /message
The endpoint that handles message-related events, such as sending and receiving messages.

### /activity
The endpoint that handles activity-related events, such as typing and activity updates.

## Events
### connection
Emitted when a user connects to the server.

### disconnect
Emitted when a user disconnects from the server.

### enterRoom
Emitted when a user joins a room.

### leaveRoom
Emitted when a user leaves a room.

### message
Emitted when a user sends a message.

### activity
Emitted when a user is typing or active in the chat room.

## Functions
### buildMsg
A function that builds a message object with the user's name, text, and timestamp.

### activateUser 
A function that activates a user and adds them to the user list.

### userLeavesApp
A function that removes a user from the user list when they disconnect.

### getUser
A function that retrieves a user object by their ID.

### getUsersInRoom
A function that retrieves a list of users in a room.

### getAllActiveRooms
A function that retrieves a list of all active rooms.

## Example Use Cases
### Joining a Room
A user joins a room and sends a message to all other users in the room.

### Leaving a Room
A user leaves a room and the server updates the user list and room list accordingly.

### Activity Updates
A user is typing in the chat room and the server emits an activity update to all other users in the room.