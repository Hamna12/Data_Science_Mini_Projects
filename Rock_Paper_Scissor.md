# Rock Paper Scissor Game

I create a game that is very popular we often play with our friends. The same thing I done with python. It is a game between User and Computer.
If user picked Rock and computer already picked it then message will appear computer picked rock and you lost. Sometimes when we Picked Paper and computer picked another
then message will appear you won. 

# Interesting

# Let's Play with me

```python
import random

user_wins = 0
computer_wins = 0

options = ["rock", "paper", "scissors"]

while True:
    user_input = input("Type Rock/Paper/Scissors or Q to quit: ").lower()
    if user_input == "q":
        break

    if user_input not in options:
        continue

    random_number = random.randint(0, 2)
    # rock:0, paper:1, scissors:2
    computer_pick = options[random_number]
    print("computer picked", computer_pick + ".")

    if user_input == "rock" and computer_pick == "scissors":
        print("You Won! ")
        user_wins += 1

    elif user_input == "paper" and computer_pick == "rock":
        print("You Won!")
        user_wins += 1

    elif user_input == "scissors" and computer_pick == "paper":
        print("You Won!")
        user_wins += 1

    else:
        print("You lost!")
        computer_wins += 1

print("You Won", user_wins, "times.")
print("The Computer Won", computer_wins, "times.")
print("Goodbye!")
```
