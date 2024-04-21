# ICMajorProject
This is our major project which comprises of a card trick and a short card game. 
# PART ONE: ARBORETUM CARD GAME
An arboretum refers to a botanical garden of trees. In this game of cards, we have 6 species (Maple, Oak, Cherry, Cassia, Willow and Poplar) each of them numbered from 1 to 8. It is a two player game. Player 1 starts the game. In the beginning, each player is randomly dealt seven cards. The first move for both players is same. Place one card in the arboretum grid and 1 card in the discard pile grid. Then in the next turn, the player is given two choices: Either take two cards from the main pile or one card from the pile and one card from the discard pile of the other player. The game runs for a total of 6 turns each for Player 1 and Player 2. The player with the most number of connected species wins the game. If there is a draw in the number of connected species between both the players, then we count the number of tree species in each player's arboretum according to an order of precedence. It goes like this: Maple>Oak>Cherry>Cassia>Poplar>Willow.
# COLLABORATORS 
Asmita De (B23CH1011), Kashish Joshi (B23CS1025)
# How to run the game
This a terminal based game so it can be run on the terminal in VS code. 
# Repositories used for reference 
https://github.com/JDSherbert/Fisher-Yates-Shuffle/commit/21885bdf0c3b956705f30ec4d263201e2417fd7a
https://gist.github.com/nups/cb05de8cccd7714eefc9
https://gist.github.com/RabaDabaDoba/145049536f815903c79944599c6f952a
# Implementation of the code
The three main parts of the game code include dealing, playing and scoring. Firstly, we defined separate structures for both the cards and the players. Within the Treecard structure we define two arrays, one for the names and the other for the numbers 1 to 8. In the Player structure, we define arrays for name, hand and 2D arrays for arboretum and discard pile. 
Using the Fisher Yates shuffling algorithm, we shuffle the cards. Then we deal 7 cards to each player using a function called deal_cards. Hand of the player is printed after each turn using the print_card function. This concludes the dealing part.
In the playing part, we implement a function called make_move which prompts the user to place one card in the arboretum (and subsequently removes the card from the player's hand by initializing it to zero) and to place one card in the discard pile(and subsequently removes that card from the player's hand). For convenience, the player places the first card in the arboretum and second card in the discard pile. Then we define another function called player_turn_with_options where the player receives a prompt to replace his/her two cards either from the main pile or 1 from pile and another from the discard pile of the other player. This is done through the use of switch case statements. Here we have also implemented error handling where if player selects a card which is not in the discard pile of the other player, then it prints that the selected card is not available. Also, player can only place a card in an index once not twice. If a player types any option other than 1 and 2, program prints 'invalid choice'. This concludes the playing part.
In the scoring part, we use the algorithm of connected components in 2D array (based on the concept of recursion)to find the consecutively connected tree cards of the same species in the arboretum of both players. Person with more number of connected components wins the game. In case of a tie, we count the different species in the players' arboretum and follow an order of precedence to determine the winner. This part involves the usage of if else statements to cover all possibilities.
# Additional features which can be added to the game
1. Add more scoring features which includes the cards in hand of the player since out of the seven cards in the beginning five cards remain the same. 
2. Adding graphics for the cards for better visualization.
3. Adding sounds to make it more appealing and fun.
4. Add more number of turns
# PART TWO: 27 CARD TRICK

