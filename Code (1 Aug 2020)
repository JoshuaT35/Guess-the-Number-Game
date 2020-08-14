print()
print("We are going to play a game. It's called, 'Guess the number!'")
print("Here's how we'll play. I generate a random number from 1 to 10,")
print("and you will have to guess it.")
print()
print("There are 3 difficulties: easy, medium or hard.")
print("The number ranges for each are as follows:")
print("EASY: 1 - 10")
print("MEDIUM: 1 - 20")
print("HARD: 1- 30")
print()

#  --  this is the difficulty selection and number generation
guessRangeList = []

import random

modeSelectList = ["EASY", "MEDIUM", "HARD"]

modeSelected = str.upper(input("Please enter your desired difficulty:  "))

while modeSelected not in modeSelectList:
    print()
    print("Oops, that's not a valid difficulty.")
    print()
    modeSelected = str.upper(input("Please type your desired difficulty:  "))

else:
    if modeSelected == "EASY":
        for num in range(1, 11):
            guessRangeList.append(num)
        randomNumber = random.randint(1, 10)

    elif modeSelected == "MEDIUM":
        for num in range(1, 21):
            guessRangeList.append(num)
        randomNumber = random.randint(1, 20)

    elif modeSelected == "HARD":
        for num in range(1, 31):
            guessRangeList.append(num)
        randomNumber = random.randint(1, 30)

print()
print("%s mode selected. You have 3 tries to guess the correct number." % (modeSelected))
###

#  --  To ask the user whether they want to to enable hints (and choose how many they want)
if modeSelected == "EASY":
    print("You have up to 3 hints.")
    hintsLeft = 3
elif modeSelected == "MEDIUM":
    print("You have up to 12 hints.")
    hintsLeft = 12
else:
    print("You have up to 21 hints.")
    hintsLeft = 21
###

#  -- To check the number of tries the player starts with and what the generated number is
#print("triesLeft")
#print(triesLeft)
#print()
#print("random number")
#print(randomNumber)

#  --  this is the guessing portion.
triesLeft = 3
numbersAlreadyGuessed = []
print()
print("Tips:")
print("1. Type 'HINT' and I will give you a number is not the correct number.")
print("2. Type 'LIST' to see your previous guesses.")
print()
userGuess = input("Can you guess the number?  ")

while userGuess != randomNumber:
#  --  If player wants to see a list
    if str.upper(userGuess) == "LIST":
        
        if len(numbersAlreadyGuessed) > 0:
            print()
            print("These numbers have been guessed already.")
            numbersAlreadyGuessed.sort()
            print(numbersAlreadyGuessed)
            print()
            userGuess = input("Can you guess the number?  ")
            
        else:
            print()
            print("You have not currently guessed any number.")
            print()
            userGuess = input("Can you guess the number?  ")
###

#  --  If player wants to use a hint
    elif str.upper(userGuess) == "HINT":
        
        if hintsLeft > 0:
            print()
            print("You used a hint.")
            numberOptions = [num for num in guessRangeList if num != randomNumber and num not in numbersAlreadyGuessed]
            hintedNumber = (random.choice(numberOptions))
            print()
            print("%d is NOT the number you're looking for: " % (hintedNumber))
            numbersAlreadyGuessed.append(hintedNumber)
            print()
            hintsLeft -= 1
            if hintsLeft > 1 or hintsLeft == 0:
                print("You have %d hints left." % (hintsLeft))
            else:
                print("You have %d hint left." % (hintsLeft))
            print()
            userGuess = input("Can you guess the number?  ")
            
        else:
            print()
            print("Sorry, you have no more hints.")
            print()
            userGuess = input("Can you guess the number?  ")
###

# if player makes a guess
    elif userGuess.isdigit() == True:

        if int(userGuess) != randomNumber:      # If player guess is wrong
            print()
            if int(userGuess) in guessRangeList:
            
                if int(userGuess) not in numbersAlreadyGuessed:     # For guessing a number they have not previously guessed
                    print("Oops, that's not the number I'm looking for.")
                    numbersAlreadyGuessed.append(int(userGuess))
                    triesLeft -= 1
                    print()     # The if loop after this determines how many tries they have left
                    if triesLeft > 1:
                        print("You have %d tries left." % (triesLeft))
                    elif triesLeft == 1:
                        print("You have %d try left." % (triesLeft))
                    else:
                        print("Sorry, you have run out of tries. The correct number was %d." % (randomNumber))
                        quit()
                else:       # If an incorrect guess or hint told the player that their guess is already not correct
                    print("Oops, you've already guessed that number.")

                print()
                userGuess = input("Can you guess the number?  ")

            else:       # If guess is not within the difficulty range
                print("Oops, that's not in the range.")
                print()
                userGuess = input("Can you guess the number?  ")

        else:       # If player guess is correct
            print()
            print("Congratulations! You guessed correctly!")
            quit()
###

#  --  If the user doesn't type 'hint', 'list' or a string solely made of intgers
    else:
        print()
        print("Sorry, I don't understand.")
        print()
        userGuess = input("Can you guess the number?  ")
###
