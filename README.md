# LaylahChessEngine
Raylah is a simple chess AI in Python that uses a positional analysis and move lookup to a specified depth to determine which moves to select. Raylah uses the python_chess module to handle the chess logic and displays the game in ASCII.

Version 0.0 was our first steps at making Raylah work in which it selects a random move from the list of legal moves and plays it. 

Version 1.0 is our next step, in which Raylah uses a basic evaluation function that rated the values of each piece corresponding to their worth (e.g a pawn had a value of 1, a knight 3, a queen 9, and a king 100) and then chose moves based on what would maximize its board's value. However, Raylah would only look one move in advance, so basically it captured the most valuable piece that it could.

Version 2.0 improves on the previous version by adding minimax and alpha-beta pruning to Raylah's evaluation, using as a heuristic the move being considered as well as the evaluation of the children of that move down to the specified depth. This version of Raylah had customizeable depth; lower depths run faster, but deeper searches produce better play. Alpha-beta pruning was added to help Raylah think faster by pruning branches that need not be considered.

Version 3.0 further develops the evaluation function. In this iteration, Raylah gained positional understanding of where certain pieces work better on a chess board. Each piece was given a 2-D array representing each square of the chess board, and each array value corresponded to the value of that square for the piece. For example, rooks should (usually) be placed towards the center rows, so the center two columns have a higher value than the edges. 
