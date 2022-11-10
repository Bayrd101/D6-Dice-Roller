# D6-Dice-Roller
# My first Python project

# dice.py

import random

def roll_dice(num_dice):

    roll_results = []
    for _ in range(num_dice):
        roll = random.randint(1,6)
        roll_results.append(roll)
    return roll_results

def parse_input(input_string):

    if input_string.strip() in {"1", "2", "3", "4", "5", "6"}:
        return int(input_string)
    else:
        print("Please enter a number from 1 to 6")
    raise SystemExit(1)

# Get and validate user's input

num_dice_input = input("How many 6-sided dice would you like to roll? [1-6] ")
num_dice = parse_input(num_dice_input) 

# Roll the Dice!
roll_results = roll_dice(num_dice)

print(roll_results) 

