# ROCK-PAPER-SCISSOR-GAME
How to Build the popular ROCK PAPER SCISSORS game with Python Programming Language.


OVERVIEW.

In the Netflix series Squid Game, players play Rock, Paper, Scissors, Minus One in the first episode of season two.


Rock, Paper, Scissors, Minus One is a deadly version of the classic game that involves players using both hands. In this variation, players show two hands, then remove one after seeing what their opponent plays. The loser of the game is subject to Russian Roulette. 


 

The game is introduced in the first episode of season two, when the mysterious recruiter, “Salesman”, gives two of Gi-hun's employees a crash course in the game. The recruiter makes the game more interesting by increasing the odds of punishment as the game continues


THE RULES OF THE GAME

According to WRPSA;

"Rock Paper Scissors (RPS) is a zero-sum game, typically played by two people using their hands and no tools. Players deliver hand signals representing rock, paper, or scissors, with the outcome determined by these three rules:

Rock wins against scissors.

Scissors win against paper.

Paper wins against rock."


THE PYTHON CODE

# ASCII Arts for rock, paper, and scissors by Paschal Mmaduabuchi

rock = '''  

    _______

---'   ____)  

      (_____)  

      (_____)  

      (____)

---.__(___)  

'''


paper = '''  

    _______

---'   ____)____  

          ______)  

          _______)  

         _______)

---.__________)  

'''


scissors = '''  

    _______

---'   ____)____  

          ______)  

       __________)  

      (____)

---.__(___)  

'''

import random

Game_images=[rock, paper,scissors]


#Now we have index the different hand gestures

#then take input from the user

Player_choice = int(input(

    "What do you choose? Type 0 for Rock, 1 for Paper, 2 for scissor. \n => "))

print("Player Choice: ")

# print game image by user choice

if Player_choice >=0 and Player_choice <=2:

  print(Game_images[Player_choice])


#just like before

#The Compute needs to pick a random number from 0 to 2

bot_choice = random.randint(0, 2)

print(" Computer's Choice: ")

# print game image by computer choice

print(Game_images[bot_choice])


# rules in logic

if Player_choice >= 3 or Player_choice < 0:

    print("You typed an invalid number, You Lose.  ☠")

elif Player_choice == 0 and bot_choice == 2:

    print("You won! 🎉")

elif bot_choice == 0 and Player_choice == 2:

    print("Sorry, you lost this round. ")

elif bot_choice > Player_choice:

    print("You lose. ")

elif Player_choice > bot_choice:

    print("You win!🎉 ")

elif bot_choice == Player_choice:

    print("It's a draw.")
