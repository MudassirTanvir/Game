# Game
#rock
"""
Rock-paper-scissors-lizard-Spock
"""

import random

# The key idea of this program is to equate the strings
# "rock", "paper", "scissors", "lizard", "Spock" to numbers
# as follows:
#
# 0 - rock
# 1 - Spock
# 2 - paper
# 3 - lizard
# 4 - scissors

# helper functions
    
def name_to_number(name):
    """
    Given string name, return integer 0, 1, 2, 3, or 4 
    corresponding to numbering in video
    """
  
    # convert name to number using if/elif/else
    # don't forget to return the result!
    if name=="rock":
        return 0
    elif name=="Spock":
        return 1
    elif name=="paper":
        return 2
    elif name=="lizard":
        return 3
    elif name=="scissors":
        return 4
    else:
        return "Error:Wrong input"
    pass
    
def number_to_name(number):
    """
    Given integer number (0, 1, 2, 3, or 4)
    corresponding name from video
    """
    
    # convert number to a name using if/elif/else
    # don't forget to return the result!
    if number==0:
        return "rock"
    elif number ==1:
        return "Spock"
    elif number ==2:
        return "paper"
    elif number ==3:
        return "lizard"
    elif number ==4:
        return "scissor"
    else:
        return "Error"
    pass


def rpsls(player_choice):
    """
    Given string player_choice, play a game of RPSLS 
    and print results to console
    """
    
    # print a blank line to separate consecutive games
    
    # print out the message for the player's choice

    # convert the player's choice to player_number using the function name_to_number()

    # compute random guess for comp_number using random.randrange()

    # convert comp_number to comp_choice using the function number_to_name()
    
    # print out message for computer's choice

    # compute difference of player_number and comp_number modulo five

    # use if/elif/else to determine winner and print winner message
    print("")
    print("Player chooses",player_choice)
    players_number = name_to_number(player_choice)
    comp_number = random.randrange(0,4)
    comp_choice = number_to_name(comp_number)
    print("Computer chooses",comp_choice)
    if (players_number-comp_number)%5 ==1 or (players_number-comp_number)%5==2:
        print("Player Wins!")
    elif (players_number-comp_number)%5!=1 or (player_number-comp_number)%5!=2:
        print("Computer Wins")
    else:
        print("Player and computer tie!")
    
    pass
     
    
# test your code
rpsls("rock")
rpsls("Spock")
rpsls("paper")
rpsls("lizard")
rpsls("scissors")

# always remember to check your completed program against the grading rubric

