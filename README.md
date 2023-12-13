# Sudoku Puzzle - Janet

## Problem Statement:
Complete the implementation of the text-based user interface to include the (as yet unimplemented and therefore failed tests) 
clear (resetting the Sudoku game), undo (a single user move, then a further move if called again and so on), save (the state of the game to a file) and load (the state of the game from a file) methods.

To design and implement a graphical user interface (GUI) for the Sudoku model code that allows the user to make moves,
undo user moves, clear (reset) the game, save to, and load from file.

## How it was implemented:
To complete the text based UI, seven methods were added to the sudoku.java class:
1. saveGameToFile
2. loadGameFromFile
3. undo
4. emptyCell
5. clear
6. resetHistory
7. getHistory

See Sudoku.java for the definition and documentation of these methods

The Graphical User Interface of the Sudoku Game comprises ;
1. ActionButtonPanel.java.java
2.  GUI.java

### ActionButtonPanel.java:
This panel contains the help, clear, undo, save and load buttons


### SudokuMain.java
This is the main class that bootstraps the sudoku puzzle by displaying the various UI options.
for the user to choose


The following methods were added to the MainGUI.java to complete the functionality of the nongram game
1. convertToVerticalString()
2. formatRowCuesString()
3. reset()
4. getButtonColor()
5. displayUserInterface()

See GUI.java for the documentation of these methods

___
### How to run the Puzzle:
___
Open the project in your favourite IDE and run the SudokuMain.java file.

This will give you the option to select either the Graphical version or the text based version of
the puzzle. You can now make moves by following the options in the text based UI or by entering the
numbers into the input box on the Graphical User Interface.

**NB: the computer generated inputs and grayed out and cannot be edited;**


### Testing
To test the functionality of the game, I added some JUnit tests to validate the correctness of the 
make move methods which was already implemented.
I also wrote tests to validate the correctness of the following methods;
1. getMoves
2. getIndividualMove
3. getGameSize
4. readLevelFile
5. isProgrammaticUpdate
6. setProgrammaticUpdate
7. checkWin
8. makeMove
9. saveGameToFile
10. loadGameFromFile
11. undo
12. emptyCell
13. clear
14. resetHistory

See the sudoku.java class for the documentation of these methods

To verify the functionality of the entire application, I tested the application against real inputs.

Below are the steps that were taken. 
I ran the SudokuMain.java and showed up the UI option screen as can be seen below;
![ui-option.JPG](sudoku_images%2Fui-option.JPG)

After clicking ok, you're presented with the 4X4 puzzle with the computer generated inputs grayed out and uneditable


#### Action Button Tests
1. Help Button test: To test the functionalities of the action buttons starting with the help button, I click on the help
which displayed the help window below;

![help.JPG](sudoku_images%2Fhelp.JPG)

2. Save Button test: To test the functionality of the save button, I entered some numbers into the puzzle and 
saved the state of the game to file. The text based UI creates a backup directory in the root
of the application and stores the saved state as sudoku_backup.txt. This is set by default to reduce the burden of 
selecting a location and file name when using the text based UI.

For the GUI, you're prompted with a window that enables you to specify the file name and location you want to save to.

The file is stored in the format below, where the * by the number indicates that the input needs to come from the user.
This enables me to distinguish computer generated values from user inputs.

**Content of Saved file**
4 -* 1 -*
3* 2 -* -*
2* -* 3 -*
1* -* -* 1

After saving the state of the puzzle, the confirmation dialogue pops up. See images below;
![save.JPG](sudoku_images%2Fsave.JPG)

![saved.JPG](sudoku_images%2Fsaved.JPG)


3. Load Button Test: To test the load functionality, press the L key to load the sudoku_backup.txt file.
For the GUI, pressing the load button pops up the file window which enables you to browse to the location 
of the file to load. You also should see  confirmation dialog when the file is loaded successfully 

See Image below
![load.JPG](sudoku_images%2Fload.JPG)

![loaded.JPG](sudoku_images%2Floaded.JPG)


4. Clear Button Test: Clicking on the clear button would prompt you to confirm your action. Upon confirming,
all user inputs will be cleared leaving on the computer generated inputs. 

![reset.JPG](sudoku_images%2Freset.JPG)


5. Quit Button Test: Clicking on the quit button would also prompt you for confirmation. Upon confirming, the 
game will quit successfully.

![quit.JPG](sudoku_images%2Fquit.JPG)


After testing the 4X4 puzzle, the difficult level was changed to hard (9X9) puzzle by changing the level and solution
file in the sudoku.java class as can be seen below;

![hard_level.JPG](sudoku_images%2Fhard_level.JPG)
![hard_level_sol.JPG](sudoku_images%2Fhard_level_sol.JPG)

The same tests were performed and the results were the same concluding that the game was working as expected.
![solved_9.JPG](sudoku_images%2Fsolved_9.JPG)



You can review the tests by viewing the SudokuTest.java file view the methods that were tested.
This file contains all the junit tests for the sudoku game.

#### Good Luck & All The Best !!!
