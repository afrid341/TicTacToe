# TicTacToe
Python OOP based TicTacToe game

TicTacToe game development process


TicTactoe is a game involving two players, where on a blank matrix of 3 X 3, each player aims to draw their individual symbol within their turns in such a manner that symbols occupy all spaces in any of the 3 rows or columns or they occupy the spaces in the diagonal of the matrix. The players can obstruct their oppositions sequence by inserting their symbols in their rows or columns or diagonal vector. If none of the above sequence is constructed by the players the game ends in a tie.

OOP development of the game by connecting the dots

Here we first try to establish individual entities of our game, the best guess is taking all the nouns as Classes, verbs of those noun as methods and their features as attributes (eg has a, or is a)

Noun 1 - Player
Noun 2 - Game (contains the Matrix or the Board)

Step 1
1. We first construct a base player class
2. The player has a symbol hence it would become the attribute, the plays a move hence it become a function
3. Thus we add an letter attribute and move function in the player Base class
4. The move function will depend upon the state of the game, hence we need to add that input to our function, lets call it game
5. Then we construct the two Player Child Classes, the computer and the human class

Step 2
1. The game TicTacToe has attributes such as a Board, decision of  the winner. Its functions would be tracking the winner, updating the board and displaying the board, reflecting the player moves with their respective letters on the board, changing the turns of the players, finding what moves are available to the players, validating if an input move is correct, validating the winning sequence for every symbol to find the winner
2. Lets start with the basic of the all, the attribute and methods involving the board 
3. The TictacToe attribute is its board, which provides the available choices or moves to the players, we construct this by making a blank list of 9 spaces
4. We can also display the board with numbers within the matrix to guide the user with their selection by utilizing the blank list
5. Lets calculate all the positions that the player can use for their move by collecting blank spaces from the board attribute

Step 3 (OOP is like a sudoku, in our process of constructing different entities of the system it can open door to relations or transactions between these entities, the goal initially may not be clear, but if we jump between each entity based on relations and continue forward the process would be much smoother)
1. Defining available moves in Tictactoe class opens connections with the Player Class, as available moves is necessary for player to do moves, hence we use this method, to generate our move.
2. First we generate a random choice for the computer from the available move list, we can store the choice in the variable for other functions
3. Next the human user is going to make an input selection through the terminal, and we can add a validation clause on the input as a wrong input such as variable or any special character (as they are not integers that would index the list) and the selection is not available in the moves list can break the flow of the program.
4. To enforce the above conditions we iterate over the inputs of the user until we get a valid selection, if the selection is valid we set it to true and breaks from the loop, to accommodate the multiple user inputs we add try and except black in the while loop

Step 4 Now we need to create an interface between the TicTacToe game and the player to setup the playing process, hence we setup play function outside different from the classes. To utilize the functions inside the game we can just write functions outside the class and use the methods inside the class
