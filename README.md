# Tictactics
=

### Database
###### Player
| Id  | Alias | Email | Password
|:-:|:-:|:-:|:-:|

- Both Email and Alias may be changed, but Alias should be unique
- Email also serves as login identifier
- SHA-256 encryption for passwords

###### Game
| Id | Gamestate | BoardState | XPlayer | OPlayer | CurrentPlayer | Winner
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|

- GameState is serialized 2Darray
- BoardState is serialized array that maps to outer-layer of Gamestate

###### GameRequest
| Id | Sender | Recipient | Accepted
|:-:|:-:|:-:|:-:|

### Server

- API to create / accept game requests
- API to create and update game state 
- Evaluates moves
- Informs on current player & game state


### Client

- Limits user to legal moves
- Informs whose turn it is
- Polls server for current game state
- Polls server for received game requests?
- Shows claimed boards (maps to board state in game)
- Facility to request match with user, that upon acceptance, starts new game
- May have more than 1 game at once?
- Stores whether request was made / and if a game is ongoing

##### Client UI
- Landing page / starting window post login is simply player list, includes facility to request a game and  notifies of requests to play
