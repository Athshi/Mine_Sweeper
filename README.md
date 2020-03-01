 - makeBoard: this function should malloc and initialize a board_t
   representing the board.  The parameters specify the width
   and height of the board, as well as the number of mines.
   You will also need to call malloc (multiple times)
   to allocate space for the 2D array "board".
   This function should fill in all squares on the board with
   UNKNOWN, then call addRandomMine an appropriate number of times
   (i.e., numMines) to "randomly" place mines on the board.
   Note that the fields of your board_t must be initailzed before
   you call addRandomMine.
   Also note that the mine generation is pseudo random and will not
   change if you re-run the program multiple times with the same
   parameters.

   Note that the layout of b->board should be such that it is indexed
     b->board[y][x]
   where y is between 0 and the height and x is between 0 and the width.

 - countMines: this funciton takes a board_t, and an (x,y) coordinate.
   It should count the mines in the 8 squares around that (x,y) 
   coordinate, and return that count.  Note that a mine may be
   indicated by a square on the board either being HAS_MINE or
   KNOWN_MINE.  You can use the IS_MINE macro to test both cases:
        IS_MINE(b->board[ny][nx]) 
   (where b is the board_t, and (nx,ny) are the coordinates you 
    want to check).  Be careful not to go out of bounds of the array.

 - checkWin: this funciton takes a board_t and see if the game has
   been won.  The game is won when no squares are UNKNOWN.

 - freeBoard: This function takes a board_t and frees all memory
   associated with it (including the array inside of it).  That is,
   freeBoard should undo all the allocations made by a call to makeBoard.