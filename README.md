# Number-Guessing-Game---PYTHON
Number Guessing Game
https://roadmap.sh/projects/number-guessing-game

import random


# MESSAGE
print("""
Welcome to the number guessing game! Here are the rules:
- The number is between 1 and 100.
- You have a set amount of chances depending on the difficulty level!
    - Easy (10 chances)
    - Medium (5 chanes)
    - Hard (3 chances) """)


level_list = ["Easy", "Medium", "Hard"]
print("")
user_attempt = True
points = 0

while user_attempt:

    r_num = random.randint(1, 10)
    difficulty_level = input("Enter your difficulty level: ")
    print("")

# EASY
    if difficulty_level.title() == level_list[0]:
        print(
            f"Alright, you have picked {difficulty_level.title()} level. You have 10 chances to guess the number! Let's start!")
        print("")
        for i in range(10):
            guess = int(input("Enter your guess: "))
            print("")
            if guess == r_num:  # RIGHT
                print(
                    f"Congratulations! the correct number was {guess}! You win!")
                print("")
                points += 10 - i
                print(f"You now have {points} points.")
                print("")
                break
            elif guess >= r_num:  # HIGH
                print(
                    f"Oops too high! Try again! You have {9 - i} attempts remaining.")
                print("")
                if i == 9:
                    break
            elif guess <= r_num:  # LOW
                print(
                    f"Oops too low! Try again! You have {9 - i} attempts remaining.")
                print("")
                if i == 9:
                    break
        attempt = input("Would you like to attempt again? ")
        print("")
        if attempt.title() == "No":
            break

# MEDIUM
    if difficulty_level.title() == level_list[1]:
        print(
            f"Alright, you have picked {difficulty_level.title()} level. You have 5 chances to guess the number! Let's start!")
        print("")
        for i in range(5):
            guess = int(input("Enter your guess: "))
            print("")
            if guess == r_num:  # RIGHT
                print(
                    f"Congratulations! the correct number was {guess}! You win!")
                print("")
                points += 5 - i
                print(f"You now have {points} points.")
                print("")
                break
            elif guess >= r_num:  # HIGH
                print(
                    f"Oops too high! Try again! You have {4 - i} attempts remaining.")
                print("")
                if i == 4:
                    break
            elif guess <= r_num:  # LOW
                print(
                    f"Oops too low! Try again! You have {4 - i} attempts remaining.")
                print("")
                if i == 4:
                    break
        attempt = input("Would you like to attempt again? ")
        print("")
        if attempt.title() == "No":
            break

# HARD
    if difficulty_level.title() == level_list[2]:
        print(
            f"Alright, you have picked {difficulty_level.title()} level. You have 3 chances to guess the number! Let's start!")
        print("")
        for i in range(3):
            guess = int(input("Enter your guess: "))
            print("")
            if guess == r_num:  # RIGHT
                print(
                    f"Congratulations! the correct number was {guess}! You win!")
                print("")
                points += 3 - i
                print(f"You now have {points} points.")
                print("")
                break
            elif guess >= r_num:  # HIGH
                print(
                    f"Oops too high! Try again! You have {2 - i} attempts remaining.")
                print("")
                if i == 2:
                    break
            elif guess <= r_num:  # LOW
                print(
                    f"Oops too low! Try again! You have {2 - i} attempts remaining.")
                print("")
                if i == 2:
                    break
        attempt = input("Would you like to attempt again? ")
        print("")
        if attempt.title() == "No":
            break
