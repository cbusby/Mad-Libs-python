# Mad-Libs-python
A python starter project to build a Mad Libs style fill in the blank game.

# Acceptance Criteria
## Main Features

Feature: User input

Scenario: A user can add a word to the story.

		Given the story needs a word
		When the user is asked for a word
		Then the user can see what to type (noun, verb, preposition, etc.)
        	And can input a word

Feature: Print

Scenario: The user can read the completed story.

		Given a Mad Libs game
		When all blank words have been filled in by user input
		Then the story is printed for the user to read
		And the game ends

## Bonus Features

Here are some bonus feature ideas you can add to make your game even better.

Feature: Download a completed story

Scenario: A user can save their story to a file once it is completed

		Given the story is filled in
		When the game ends
		Then a .txt file is saved containing the finished story

Feature: Default suggestions

Scenario: A user can press enter with no input and the Mad Libs game will print a story with a default word

		Given a user is prompted to input a word
		When the user presses the Enter key without any input characters
		Then the Mad Libs game provides a default answer

		Given a default answer was inserted into the story
		When the story is printed for the user to read
		Then the user can see the default word in the story

Feature: Print an error message

Scenario: A user accidentally types a character that does not make sense like “@”,”$”,”^”, or, “?”. The game gives an error message to let the user know of their mistake.

		Given a user is prompted to input a word
        	When a user has input an illegal character
		Then the game prints an error message “Illegal character in string. Please input a new word.”
		And the game reprompts them to input a word

Feature: Import new stories into your game

Scenario: On start of the program, the game can read in a story from a file.

		Given a file with a formatted story
		When the game starts
		Then the game can import the story from the file
		And the user can add words to this story to play the game

Feature: Define a part of speech

Scenario: A user is asked for a preposition but they forgot what that is. The can type “--help” and the part of speech is defined.

		Given a user is prompted to input a word
		When the user inputs “--help”
		Then the game prints the definition of the part of speech
		And asks the user to input the word once more

Feature: Choose a story to play

Scenario: On start of the program, the game lists titles of stories to play. The user can select which story they would like to play.

		Given there are multiple stories to play
		When the game starts
		Then the titles of stories are printed in a menu
		And the user is prompted to type in the number of the story they would like to play

		Given the user has selected a story
		When all blank words have been filled in by user input
		Then the story the user selected is printed to read
		And the game ends

Feature: Select a random story

Scenario: On start of the program, the game selects a story randomly from several options.

		Given there are multiple stories to play
		When the game starts
		Then a random story is selected for the user to play

Feature: Add a game loop

Scenario: Create a game loop where once a story is complete, the program starts again. The user can enter “exit” as a command to end the game at any point.

		Given the game starts
		When a story is completed
		And the story is printed out for the user to read
		Then getting words from the user starts again

		Given the user is asked for a word
		When the user inputs “exit”
		Then the game ends immediately
