Binar Challenge Chapter 7 Fullstack Web

# How to use :

- <code>sequelize-cli db:migrate</code>
- <code>sequelize-cli db:seed:all</code>
- <code>npm start</code>
- Login as admin to access admin dashboard
  - Username : admin
  - Passwrod : admin

# User Table (User, Biodata, History)

Access using admin token.

- Get all users : GET <code>/api/v2/users</code>
- Get a user : GET <code>/api/v2/user/:id</code>
- Create user : POST <code>/api/v2/auth/register</code>
- Edit a user : PUT <code>/api/v2/user/edit/:id</code>
- Delete a user : DELETE <code>/api/v2/user/delete/:id</code>

# Room Table

Access using admin token.

- Get all room : GET <code>/api/v2/rooms</code>
- Get a room : GET <code>/api/v2/room/:room</code>

# Games

Login using user auth token or insert username & password.

- Login user : POST <code>/api/v2/auth/login</code>
- Check your token : GET <code>/api/v2/whoami</code>

Room always created by player one, and player two must join the room, access this endpoint using player or admin token.

- Create a room : POST <code>/api/v2/room/create</code>

  Player one create a room.

- Join room : POST <code>/api/v2/room/:room/join</code>

  Player two join a room that has not yet started and created by player one.

- Play in room : POST <code>/api/v2/room/:room/play</code>

  Each player need to insert their username and picks on each endpoints to play created room by player one.

- Get room result : GET <code>/api/v2/room/:room/result</code>

  Get the result of each round by insert round from 1 - 3.
