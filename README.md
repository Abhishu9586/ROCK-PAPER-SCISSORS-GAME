# ROCK-PAPER-SCISSORS-GAME
ROCK-PAPER-SCISSORS GAME with the help of python

#Rock-paper-scissors Game 

import random

#game rule

print('Winning rules of the game ROCK PAPER SCISSORS are :\n'
      + "Rock vs Paper -> Paper wins \n"
      + "Rock vs Scissors -> Rock wins \n"
      + "Paper vs Scissors -> Scissor wins \n")

#choose choice by user

while True:
    print("Enter your choice \n 1 - Rock \n 2 - Paper \n 3 - Scissors \n")
    choice = int(input("Enter your choice : "))

    while choice > 3 and choice < 1:
        print("Enter a valid choice please...")
    
    if choice == 1 :
        user_choice = "Rock"
    if choice == 2:
        user_choice = "Paper"
    if choice == 3:
        user_choice = "Scissors"
    if choice >= 4:
        print("enter valid choice")
        break
    
    #printing user's choice
    
    print("User choice is : ", user_choice)
    print("Now it's Computers Turn...")

    #computer choise
    
    choice_names = ["Rock","Paper","Scissors"]
    comp_choice = random.choice(choice_names)

    
    print(f"Computer choice is : {comp_choice}")
    print(user_choice, "Vs", comp_choice)

    #obtaining the result 
    
    if comp_choice == user_choice:
        result = "It's Draw => It's a tie"

    if (comp_choice == "Paper" and user_choice == "Rock"):
        result = "Paper wins => Computer wins"
    elif (comp_choice == "Paper" and user_choice == "Scissors"):
        result = "Scissors wins => User wins"

    if (comp_choice == "Rock" and user_choice == "Paper"):
        result = "Paper wins => User wins"
    elif (comp_choice == "Rock" and user_choice == "Scissors"):
       result = "Rock wins => Computer wins "

    if (comp_choice == "Scissors" and user_choice == "Paper"):
        result = "Scissors wins => Computer wins"
    elif (comp_choice == "Scissors" and user_choice == "Rock"):
        result = "Rock win => User wins"
    
    #Printing the result
    
    print(result)
    
    #if the user want to play again
    
    print("Do you want to play again..? (Y/N)")
    answer = input()
    if answer == 'n':
        break
    
print("Thanks for Playing...*")
