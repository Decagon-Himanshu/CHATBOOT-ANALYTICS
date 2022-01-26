#using Random module puzzle game
import random
randNumber = random.randint(1,546465)
print(randNumber)
userGuess = None
Guesses = 0

while(userGuess!=randNumber ):
    userGuess = int(input("Enter the number:"))
    Guesses +=1
    if(userGuess==randNumber):
        print("you gusses is right")
    else:
        if(userGuess>randNumber):
            print("you guess its wrong ! Enter a smaller number")
        else:
            print("you guess its wrong ! Enter a larger number")
print(f"You guesses the number in {Guesses} guesses")
with open("hiscore.txt","r") as f:
    hiscore = int(f.read())

if(Guesses<hiscore):
    print("you have just broken the high score")
    with open("hiscore.txt", "w") as f:
        f.write(str(Guesses))

