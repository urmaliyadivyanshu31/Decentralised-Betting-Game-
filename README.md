# Decentralised-Betting-Game-
Here’s a brief explanation of each function in the code:

1. **createGame**: This function allows the owner of the contract to create a new game with a specified ID and description. It sets the game state to GameState.OPEN.
2. **placeBet**: This function allows a user to place a bet for a specific game ID and bet ID. The user must send the amount of Ether they wish to bet as the transaction value. The function checks that the game and bet IDs are valid and that the bet is open for placing bets. It then stores the user's bet and the amount of Ether they bet in a mapping.
3. **removeBet**: This function allows a user to remove their bet for a specific game ID and bet ID. The function checks that the game and bet IDs are valid and that the bet is open for placing bets. It then removes the user's bet and refunds the amount of Ether they bet.
4. **closeBet**: This function allows the owner of the contract to close a specific bet for a specific game ID. Once a bet is closed, no more bets can be placed for that bet ID in the game. The function checks that the game and bet IDs are valid and that the bet is open for closing bets. It then sets the bet state to BetState.CLOSED.
5. **closeGame**: This function allows the owner of the contract to close a specific game. Once a game is closed, no more bets can be placed or removed, and no more bets can be closed. The function checks that the game ID is valid and that the game is open for closing. It then sets the game state to GameState.CLOSED and transfers all the funds in the game to the owner of the contract.
6. **declareWinners**: This function allows the owner of the contract to declare the winners for a specific game. The owner specifies an array of winning bet IDs for the game. The function checks that the game ID is valid and that the game state is GameState.WAITING_FOR_WINNERS. It then sets the game state to GameState.WINNERS_DECLARED and distributes the winnings to the users who placed winning bets. The winnings are transferred to the users' addresses through the transfer function.

