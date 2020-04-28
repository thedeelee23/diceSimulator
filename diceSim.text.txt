''' Author: Dillon Lee
Created April 27th 2020
This application simulates the roll of multiple different types of dice'''


import random
import os
clear = lambda: os.system('cls')

def roll_dice(diceSides):
	
	diceA=random.randint(1,diceSides)
	print('You rolled a :' + str(diceA))
	rollMore=input("Roll again? (y/n) or 'c' for change die: ")
	roll_again(rollMore[0],diceSides)
	
def roll_again(select, diceSides):
	if select == "y":
		
		roll_dice(diceSides)
		
	else: 
		mainScreen()
		
def mainScreen():
	
	clear()
	diceSideNum= input("Enter many faces does your die has: ")
	roll_dice(int(diceSideNum))
	
mainScreen()
	
	