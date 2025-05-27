# COM-S-327-Programming-Project-1.05-User-Interface-with-Ncurses-solved

Download Here: [COM S 327 Programming Project 1.05 User Interface with Ncurses solved](https://jarviscodinghub.com/assignment/programming-project-1-05-user-interface-with-ncurses-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

Last week we added some characters, and made them move around and smite one another. You added
some code to drive your @. You can rip that code out, now1
. We’re going to add a user interface that you can
use to drive your @ manually. If you like, you can leave the auto-drive code in there and add a command to
turn it on and off at runtime.
Still working in C, link in the ncurses library and use it for unbuffered I/O and to draw only a portion of
your dungeon roughly centered on the PC. Handle recentering however you like—every turn, when the PC
gets too close to the edge, etc.—but now you only draw an 80 × 21 portion of the dungeon that contains the
PC.
Since we are only drawing a portion of the dungeon, we want to be able to look around, so we’re adding
a look mode in addition to PC control, which we’ll call control mode.
We’re going to add stairs now, too. When the PC goes up or down a staircase, a new dungeon is
generated and populated with the PC and new monsters. An upward staircase is represented with <; a downward staircase with >. The PC uses stairs by entering the appropriate stair command while standing
on the staircase. NPCs cannot use stairs, not even the smart ones. Stairs provide an important means of
escape for PCs.
All commands are activated immediately upon key-press. There is never a need to hit enter. Any
command which is not explicitly defined is a no-op. Implement the following commands:
Key(s) Action
7 or y In control mode, attempt to move PC one cell to the upper left.
8 or k In control mode, attempt to move PC one cell up. In look mode, attempt to move the view
pane up by no more than one window height.
9 or u In control mode, attempt to move PC one cell to the upper right.
6 or l In control mode, attempt to move PC one cell to the right. In look mode, attempt to move
the view pane to the right by no more than one window width.
3 or n In control mode, attempt to move PC one cell to the lower right.
2 or j In control mode, attempt to move PC one cell down. In look mode, attempt to move the
view pane down by no more than one window height.
1 or b In control mode, attempt to move PC one cell to the lower left.
4 or h In control mode, attempt to move PC one cell to the left. In look mode, attempt to move the
view pane to the left by no more than one window width.
5 or space In control mode, rest for a turn. NPCs still move.
> In control mode, attempt to go down stairs.
< In control mode, attempt to go up stairs.
L In control mode, enter look mode.
escape In look mode, enter control mode. Return view to PC’s position.
Q Quit the game.
With these changes, we no longer need the delay that we built in last week; the game pauses automatically for input. And ncurses should handle the redrawing, so we’re no longer spewing the entire dungeon to
the terminal each turn. Things will look much nicer.
Our dungeons will use 21 out of 24 lines in a terminal. Display them on lines 1–21 (zero indexed). The
top line is for message display. Use it to display any messages you like (like debugging information!). The
bottom 2 lines are for status information, which we’ll deal with in a later assignment.
You may add any other commands that you like, or map the required commands to additional keys,
as long as you implement the specified mappings. If you choose to add other commands or mappings,
please be aware that future assignments will specify additional commands and you may need to change
your mappings. Future required commands will be limited to lowercase letters; therefore, you may choose
uppercase letters, punctuation, control- and alt- modified keys, etc., without danger of future assignments
forcing a change.
1
If you gave your PC any special powers, like the ability to tunnel through walls, those should no longer apply, either.
