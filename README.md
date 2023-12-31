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
This panel contains the help, clear, undo, save, quit, and load buttons.

___
### How to run the Puzzle:
___
Open the project in your favourite IDE and run the GUI.java class for the Graphical User Interface or
the UI.java class for the text-based version of the puzzle. 

You can now make moves by following the options in the text-based UI or by entering the
numbers into the input box on the Graphical User Interface.

**NB: the computer-generated inputs and grayed out and cannot be edited;**


### Testing
To test the functionality of the game, I added some JUnit tests to validate the correctness of the 
make move methods that were already implemented.
I also wrote tests to validate the correctness of the following methods;
1. getMoves
2. getIndividualMove
3. getGameSize
4. readLevelFile
5. isProgrammaticUpdate
6. makeMove
7. saveGameToFile
8. loadGameFromFile
9. undo
10. emptyCell
11. clear
12. resetHistory

See the sudoku.java class for the documentation of these methods

To verify the functionality of the entire application, I tested the application against real inputs.

Below are the steps that were taken. 

I ran the GUI.java pops up the 4X4 GUI puzzle with the compute-generated inputs grayed out and uneditable
![4_4.JPG](sudoku_images%2F4_4.JPG)

#### Action Button Tests
1. Help Button test: To test the functionalities of the action buttons starting with the help button, I click on the help
which displayed the help window below;

![help.JPG](sudoku_images%2Fhelp.JPG)

2. Save Button test: To test the functionality of the save button, I entered some numbers into the puzzle and 
saved the state of the game to file. The text-based UI creates a backup directory in the root
of the application and stores the saved state as sudoku_backup.txt. This is set by default to reduce the burden of 
selecting a location and file name when using the text-based UI.

For the GUI, you're prompted with a window that enables you to specify the file name and location you want to save to.

The file is stored in the format below, where the * by the number indicates that the input needs to come from the user.
This enables me to distinguish computer-generated values from user inputs.

**Content of Saved file** <br/>
4 -* 1 -* <br/>
3* 2 -* -* <br/>
2* -* 3 -* <br/>
1* -* -* 1 <br/>

After saving the state of the puzzle, the confirmation dialogue pops up. See images below;
![save.JPG](sudoku_images%2Fsave.JPG)

![saved.JPG](sudoku_images%2Fsaved.JPG)


3. Load Button Test: To test the load functionality, press the L key to load the sudoku_backup.txt file.
For the GUI, pressing the load button pops up the file window which enables you to browse to the location 
of the file to load. You also should see the confirmation dialog when the file is loaded successfully 

See Image below
![load.JPG](sudoku_images%2Fload.JPG)

![loaded.JPG](sudoku_images%2Floaded.JPG)


4. Clear Button Test: Clicking on the clear button prompts you to confirm your action. Upon confirming,
all user inputs will be cleared leaving on the computer-generated inputs. 

![reset.JPG](sudoku_images%2Freset.JPG)


5. Quit Button Test: Clicking on the quit button prompts you for confirmation. Upon confirming, the 
game will then quit successfully.

![quit.JPG](sudoku_images%2Fquit.JPG)

6. Upon making all the right moves to complete the puzzle, you should see a pop-up confirming that you've solved the puzzle
successfully as can be seen below;

![solved.JPG](sudoku_images%2Fsolved.JPG)

After testing the 4X4 puzzle, the difficult level was changed to hard (9X9) puzzle by changing the level and solution
file in the sudoku.java class as can be seen below;

![hard_level.JPG](sudoku_images%2Fhard_level.JPG)
![hard_level_sol.JPG](sudoku_images%2Fhard_level_sol.JPG)

The same tests were performed and the results were the same concluding that the game was working as expected.
![solved_9.JPG](sudoku_images%2Fsolved_9.JPG)



You can review the tests by viewing the SudokuTest.java file view the methods that were tested.
This file contains all the junit tests for the sudoku game.

#### Good Luck & All The Best !!!
