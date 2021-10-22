# Chess
# 2-Player Chess

Worth 100 points (10% of course grade.)

For this assignment you will explore how to apply the object-oriented design ideas you learned in class to design and implement the chess game.

You will work in pairs on this assignment. Read the [DCS Academic Integrity Policy for Programmming Assignments](http://www.cs.rutgers.edu/academics/undergraduate/academic-integrity-policy/programming-assignments) - you are responsible for this. In particular, note that **"All Violations of the Academic Integrity Policy will be reported by the instructor to the appropriate Dean"**.

IMPORTANT: Note that you will be maintaining your code in [Bitbucket](https://bitbucket.org/), which is a source code repository. Learning how to manage your source code INCREMENTALLY and in COLLABORATION with your project partner is an important skill, and Bitbucket (like GitHub) is a code repository that allows you to do this effectively. Read the last section on Submission for more details.

---

You will implement the game of [Chess](http://en.wikipedia.org/wiki/Chess) for two players. Your program, when launched, should draw the board in text, on the terminal and prompt whomever's turn it is (white or black) for a move. Once the move is executed, the move should be played and the new board drawn, and the other player queried.

---

## Output

The board should be drawn on the screen with ascii art **EXACTLY** as shown in this [example](display.txt). Note there is a blank line above and below any prompt/message your program will print, and the board itself. Deviations from this exact format will incur a penalty.

**You will NOT use a graphical user interface**, that is not the point of this assignment. If you do, your submission will NOT be graded.

**You MUST have white make the first move**. Having black make the first move is not appropriate, and will incur a penalty.

If you are not clear about any of this, or have ANY questions or issues, CHECK with your grader.

Note:

-  Every piece must know what moves are allowed on it. If a player attempts an illegal move on a piece, your program should not execute the move. Instead, it should print `"Illegal move, try again"`, followed by the usual prompt (for white's move or black's move).
-  When a move is made, and it puts the opponent's King under check, your program should print `"Check"` before prompting for the opponent's move.
-  If a checkmate is detected, your program should print `"Checkmate"`
-  The last thing before termination should be a display of `"Black wins"`, `"White wins"` or `"draw"`.

## Input

Your program needs to accept input of the form `"FileRank FileRank"`, where the first file (column) and rank (row) are the coordinates of the piece to be moved, and the second file and rank are the coordinates of where it should end up. (See the board example shown above.)

The figure immediately below should make it clear which rank and file combinations belong to which squares. The white pieces always intially occupy ranks `1` and `2`. The black pieces always initially occupy ranks `7` and `8`. The queen always starts on the `d` file.

![Chess Example](img/SCD_algebraic_notation.svg)

As an example, advancing the white king's pawn two spaces would be input as `"e2 e4"`.

A castling move is indicated by specifying where the king begins and ends. So, white castling king's side would be `"e1 g1"`.

A pawn promotion is indicated by putting the piece to be promoted to after the move. So, promoting a pawn to a knight might be `"g7 g8 N"`. If no promotion piece is indicated, it is assumed to be a queen.

[Example of black winning](ex1.txt)

## Ending the game

If checkmate occurs, the game shall end immediately with the result reported.

A player may resign by entering "resign".

-  [Example of white resigning](ex_res_w.txt)
-  [Example of black resigning](ex_res_b.txt)

A player may offer a draw by appending `"draw?"` to the end of an otherwise regular move. The draw may be accepted by the other player submitting `"draw"` as the entirety of his or her next move. There will be no automatic draws (due to unchanging positions over long periods of time, etc).

-  [Example of a draw](ex_draw.txt)

**You are NOT required to implement termination by threefold repetition, or the fifty-move rule**. (You are welcome to include them in your code to make it complete; however, there is no extra credit for either.)

