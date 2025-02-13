
1. Contract Creation (Lottery)

The contract is deployed by a manager (the creator).
The manager has special permissions to pick a winner.

2.Entering the Lottery (enter())

Players can join the lottery by sending more than 0.01 Ether.
Their address is stored in the players array.

3.Generating a Random Winner (random())

Uses block difficulty, timestamp, and players array to generate a pseudo-random number.
Not truly random and can be manipulated.

4.Picking the Winner (pickWinner())

Only the manager can call this function.
The winner is chosen using the random() function.
The entire contract balance is sent to the winner.
The players array is reset for the next round.

5.Restricted Access (modifier restricted)

Ensures only the manager can call pickWinner().

6.Getting Players (getPlayers())

Returns the list of participants.
