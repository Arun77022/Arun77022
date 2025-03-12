import sys
import random
from enum import Enum

class RPS (enum):
    ROCK=1
    PAPER=2
    SCISSOR=3
    


print("")
pc = input(                                                        "Enter...........\n1 for rock,\n2 for paper,or \n3 for scissor:\n\n")

print(pc)
print(type(pc))
    
    
player = int(pc)

if player<1 or player >3:
    sys.exit("you must enter 1,2,and 3.")

cc = random.choice("123")

computer=(int(cc))

print("")
print("you chose"+str(RPS(pc)).replace('RPS.','')+".")
print("python chose "+str(RPS(cc)).replace('RPS.','')+".")
print("")

if player == 1 and computer == 3:
    print("🎉😖🎉 you win!")
    
elif player == 2 and computer == 1:
    print("🎉😖🎉 you win!")
    
elif player == 3 and computer == 1:
    print("🎉😖🎉 you win!")
    
elif player == computer:
    print("☹️ tie game!")
    
else:
    print("🎉😖🎉 python win!")
