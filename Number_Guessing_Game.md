# Number Guessing Game

I create a game that will show you make a correct guess of number or not. If you make a guess then message will display either you are above the guess or below the guess.
And if we enter any alphabet or negative number then message will appear Please enter a number next time.
# Interesting

# Let's Play with Me

```python
import random

top_of_range = input("Type a number: ")

if top_of_range.isdigit():
    top_of_range = int(top_of_range)

    if top_of_range <= 0:
        print("Please type a number larger than 0 next time.")
        quit()

else:
    print("Please type a number next time.😞")
    quit()

random_number = random.randint(0, top_of_range)
guesses = 0

while True:
    guesses += 1
    user_guess = input("Make a guess: ")
    if user_guess.isdigit():
        user_guess = int(top_of_range)
    else:
        print("Please type a number next time.😞")
        continue

    if user_guess == random_number:
        print("Yeah You Got it! 🥳")
        break
    else:
        if user_guess > random_number:
            print("You were above the number!")
        else:
            print("You were below the number!")

print("You got it in ", guesses, "guesses")
```
