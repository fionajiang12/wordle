CIS 1200 Game Project README
=:=:=:=:=:=:=:=:=:=:=:=:=:=:=:=:=:=:=

===================
=: Core Concepts :=
===================

- List the four core concepts, the features they implement, and why each feature
  is an appropriate use of the concept. Incorporate the feedback you got after
  submitting your proposal.

  1. 2D Arrays
  I used 2D Arrays to implement the board to store each letter and their corresponding states.
  This is an appropriate use of the concept because each position in the array is a Tile class object.
  Using 2D Arrays, I can accurately store the game board since it is in the form of a grid.

  2. Collections
  I used collections to store all the 6 letter english words and act as a word bank. This comes from the feedback
  I got after submitting my proposal. I used TreeSet to store the words because each word only occurs once and there
  are no identical words in a word bank. Every time when I want to choose a word in the word bank, it is easy
  to retrieve the word.

  3. File I/O
  I used File I/O in two places.
  First, I used it to read the txt file that stores all the 6-letter words. Because each word is right next
  to each other with a space in between, it is easy to iterate through the file with File I/O.
  Then, I used it to save and restore the game state. I stored all the current game states into a file called
  gamestate.txt. When the restore function is called, the program will read from the text file. It is an appropriate
  use of File I/O.

  4. JUnit Testable Component
  I designed the model to be independent from the GUI components so that it can run without the GUI interface.
  I individually designed functions to deal with checking valid word, picking word, assigning states to each time,
  and many other functions.

=========================
=: Implementation :=
=========================

- Provide an overview of each of the classes in your code, and what their
  function is in the overall game.
  I have four classes in total.
  The first class is RunWordle. This class takes care of running the game including showing the instruction window,
  and the main game window.
  The second class is GameBoard. This class is responsible for showing the letters that are typed in and the
  corresponding colors of each letter once it is entered. It also has a key listener that listens to actions on
  keyboard such as typing a letter or pressing enter or delete and act accordingly.
  The third class is Wordle. This is the main class for the game model that contains all the game functions such as
  checking valid words, adding tiles to the board and so on. It incorporates all functionalities of wordle that it can
  function without the GUI components.
  The last class is Tile. It is a class that represents each individual tile on the board. It contains the letter of
  the tile, the current state (0 for the default, 1 for gray blocks, 2 for yellow blocks, and 3 for green blocks),
  and the current column and rows. The 2D array is constructed with Tile class objects.
