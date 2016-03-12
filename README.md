# Odds-and-Evens

This solidity contract faciliates a game of odds and evens but also especially with a function(claim or refund) that is described here: http://people.csail.mit.edu/ranjit/papers/poker.pdf

The first player to "choose" (and enter a bet) has until the other player "chooses" to refund their own (player one's) initial deposit.  Once player two "chooses" each player MUST "reveal" their choices, in the reveal round, in order to have a chance at getting their deposit back (and to possibly win or claim the other players deposit).  If a player enters a choice, they will automatically lose their deposit to the other player, if they don't later reveal their otherwise encrypted chocie. In a situation where one player doesn't reveal, the player that DOES reveal can claim both deposits.

The purpose of the claim or refund primitive is such that each player can decide to enter a bet without having to reveal their choice.  Only when BOTH players have deposited and made their choice are they asked to reveal. 

The two important features are:

1) There is no fear of playing versus another player that hasn't deposited.

2) No malicious player can profit, by forcing an honest player to reveal their choice, while not revealing their own.



