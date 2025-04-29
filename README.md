import random
'''
1 for sanke
-1 for water 
0 for gun
'''

computer = random.choice([-1,0,1])
youstr = input("Enter your choice:")
youDict = {"s" : 1, "w" : -1, "g": 0}
reverseDict = {1: "snake", -1: "water", 0: "gun"}

you = youDict[youstr]

# By now we have 2 numbers (variable), you and computer

print(f"You chose {reverseDict[you]}\n computer chose {reverseDict[computer]}")

if(computer == you):
    print("It's a draw")

else:
    if(computer == -1 and you == 1):
        print("you Win!")

    elif(computer == -1 and you == 0):
        print("you Loss!")

    elif(computer == 1 and you == -1):
        print("you Loss!")

    elif(computer == 1 and you == 0):
        print("you Win!")

    elif(computer == 0 and you == -1):
        print("you Win!")

    elif(computer == 0 and you == 1):
        print("you Loss!")
    else:
        print("Something went wrong!")
