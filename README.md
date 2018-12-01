# N-Rooks and N-Queens
Both the problem, that are being solved here, are similar. The main idea here is to arrange N-pieces(rooks or queens) on a board of size NxN such that no piece is attacking any other piece on the board. There's also an option to specify positions on board that are unavailable, that is, a piece cannot be placed in those positions.

## Input:
The program takes three inputs and some additional inputs based on value of 3rd argument:
1. Problem Type: Specifies the type of problem. It can take two values, nqueen for solving nqueens problem and nrook for solving nrooks problem.
2. N: Size of the board
3. Number of unavailble positions on board. If this value is not 0 then other additional arguments must be given to specify the board positions which are unavailable in the following form: row_number space column_number.
For example: nqueen 7 2 1 1 7 7 would tell the program to solve N-Queens problem for a board size of 7x7 such that the top-left and bottom-right squares are unavailable.

## Output:
The output of the program is a NxN board with a 'R' indicating a rook(for N-Rooks problem), 'N' indicating a queen (for N-Queens problem), '\_' indicating an empty square and 'X' indicating an unavailable position.

# N-ROOKS
The N-Rooks problem is solved by expoiliting the valid moves for a rook on a chess board. Since, rooks can only attack a piece that is the same row or column as them, the easiest way to solve N-Rooks is to put all the pieces in a diagonal or somewhere near the diagonal if a position in the diagonal is unavailable.

# N-Queens
The N-Queens puzzle problem is solved using a backtracking algorithm. At each iteration, one queen is placed on the board until a goal state is found or no more position is left on the board where a piece can be placed without violating the constraints of the problem. If a goal state is found, then the solution is returned and the board is printed. For later, the algorithm backtracks to one of the earlier board states and continues from there in some direction other than the one it took before, which resulted in a dead-end. I have used Depth First Search algorithm to implement backtracking. The program can find solution for any value other than N=2 and N=3 because for those board sizes, no solution exists for N-Queens problem.
