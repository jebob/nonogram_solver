# nonogram_solver
Small tool for solving nonograms

https://github.com/tsionyx/nonogrid is better if you have a real need to solve Nonograms, but this is my attempt.


## Usage instructions
To solve a puzzle from [Brainbashers](https://www.brainbashers.com/nonogrids.asp), copy/paste the grid into a text file
To solve a puzzle from [webpbn](https://webpbn.com), go to https://webpbn.com/XMLpuz.cgi?id={puzzle_id} and save that xml as a file.

Produces output like

```
Solving Examples/Medium2.txt
XX XXXXX    XX   XXXXXXXX
X   XXXX     X   X  XXXXXXX
      X              XX XXX
   XX          XX    X   XX
   XX     XX   XX X      X
XXXXX     XXX  XXXX      X
XXXXX  XX  XX  XXXXX     XXX
XXXXX      XXXXXXXXX   X XXXXX
XXX X X X XXX XXX X   XX XXXXX
        XXXXXXXXXXX  XXXXXXXXX
X       XXXXX  XXX       XXXX
X       XXXXX   XX X X XXXXXX
XXX XXXXXXXXX   XX X   XXXXX
XXXX  XXXXXXXX   XXXX XXXXXXXX
XXXX  XXXXXX  X   XXXXXXXXXXXX
XXXX   XXX X     XXXXXXXXXXXXX
XXXX    X           XX X XXXXX
 XXX    X   XXXX  XXX      XXX
 XXX     XXXXXXXXXXXXX    XXXX
   X    XXXXXXXXXXXX X    XX
   XX   XXX  XXX   X      XXX
         X    XX   XX    XXX
         XX    X   X     XXXX
        XXXX       XXXXX XXXXX
   XXXXXXXXX         XXXXXXXXX
       XXX X X    XXXXX   XXXX
X  X XXXXX      XXXXXXXX XXX
X      XXX     XXXXXXXX   XX
        XXX   XXX X X    XXX
        XXXX XXX  X X    X X
```

With ` ` (blank space) for whites, `X` for blacks, `?` for unknowns.

## Limitations
This solver examines every possible solution for each line. This has two limitations:
* This is insufficient to solve all cases. Backtracking can solve all cases given enough time but I haven't implemented this yet.
* This can be very slow on larger puzzles where a single line can have many combinations. The next step towards speeding this up is detecting when no further deductions are possible.
