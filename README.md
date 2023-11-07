# Introduction

I had an idea to make an MMO-type, browser-based game in which users control a porpoise avatar. All users are in the same massive server.

Similar to slither.io or agar.io in terms of being massively multiplayer. For reference slither.io used Node.js and socket.io for client-server communication. But it seems like socket.io restricts you to a Node.js server, and I was considering implementing the server in Rust. (this might help: https://github.com/Totodore/socketioxide)

## To-do


## Gameplay

Users will interact with the game through the arrow keys and a text box. The camera is fixed top-down, and arrow keys simply move the porpoise avi in 4 directions.

The key feature is the text box, which is a prompt for users to enter something that gives them purpose. Purpose in this is defined as "something that gives you meaning, joy, or pride."

For example, let's say the user enters "creativity" meaning the act of creating something (i.e. art or music) gives them meaning. There are two possible cases:
1. "creativity" does not exist in the database, we create a new "landmass" dedicated to "creativity" and the user is moved to that part of the map
   1. landmasses will be indicated by a "castle" icon on the map
2. "creativity" does exist in the database, we move the user's avi to the existing "landmass"

## Navigating the codebase

`/client`: Javascript client code, using socket.io
`/server`: Rust server code, using socketioxide

## References
https://github.com/Totodore/socketioxide
https://socket.io/
