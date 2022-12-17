# Gomoku

The goal of this project is to make an AI capable of beating human players at Gomoku.

## Additional Gomoku Rules

- The game ends when one player manages to align five stones. Sometimes, only an alignment of 5 can win, and sometimes 5 or more is okay. In the context of this projet, **we will consider 5 or more to be a win**.

- Gomoku will be played on a 19x19 Goban, without limit to the number of stones.

- Capture (As in the Ninuki-renju or Pente variants) : You can remove a pair of your opponent’s stones from the board by flanking them with your own stones. 
This rule adds a win condition : **If you manage to capture ten of your opponent’s stones, you win the game.**

- Game-ending capture : A player that manages to align five stones only wins if the opponent can not break this alignment by capturing a pair, or if he has already lost four pairs and the opponent can capture one more, therefore winning by capture. There is no need for the game to go on if there is no possibility of this happening.

- No double-threes : It is forbidden to play a move that introduces two free-three alignments, which would guarantee a win by alignment.

## Project Guidelines

- Free to use whatever language and graphical interface.

- Should not crash in any circumstances.

- Makefile with rules `$(NAME), all, clean, fclean and re`

- Use **minimax** algorithm (or an alternative) and write a custom heuristic.

## Validation 

- AI takes an average  of <= 500ms to find a move.