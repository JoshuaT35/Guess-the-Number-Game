# What is this game?
This is a guess-the-number game written in Python, as the name aptly states. A number is generated within a range of numbers (including the end numbers), and the player must correctly guess the correct number. They have a limited number of guesses, so hopefully luck is on their side today! It's my first game, so its existence and functionality is already a milestone for me. 

# Current Features (30 Mar 2021):
1. Currently with over 200 lines of code (some of the lines are from in-line spacing for stylistic purposes, leading to a total of 177 used purposefully)
2. Option to select between 3 difficulties (Easy, Medium and Hard: the number-guess-range increases by increments of 10, beginning from 1-10)
3. Option to use hints (As difficult increases, the number of hints available to the player increases by 9)
4. Option to see a list of numbers that have already been guessed or hinted at
5. Option to ask the player if they want to play again
6. Dialogue is available for all possible results when the player makes certain choices. There is dialogue for wanting to see an empty list, wanting to use hints even if there are none left, etc.


Ideas I implemented:
1. Used while loops so that a player would eventually give a certain response to every question ask
2. Replaced multiple print() lines with 1 print() command and /n throughout to reduce the number of commands
3. A user-friendly quit option was written by making the computer wait for a few seconds before actually quitting. That way, the quit wasn't instantaneous.
4. Encapsulated most of the code in a function. This way, the game can repeat just by calling that function
