### Code:
```py
print("-------------------------Welcome To jug problem---------------------------")
print("Given two water jugs with capacities 4 and 3 litres. Initially, both the jugs are empty. Also given that there is an infinite amount of water available. The jugs do not have markings to measure smaller quantities. One can perform the following operations on the jug:")
print("1. Fill Jug 1 completely (4 ltr)")
print("2. Fill Jug 2 completely (3 ltr)")
print("3. Transfer water from Jug 1 to Jug 2")
print("4. Transfer water from Jug 2 to Jug 1")
print("5. Empty Jug 1")
print("6. Empty Jug 2")
print("The task is to determine whether it is possible to measure 2 litres of water using both jugs.")

jug1 = 0
jug2 = 0

while True:
    if jug1 == 2 or jug2 == 2:
        print("Congratulations!!! You won")
        break

    else:
        print("Select Your Option: ")
        choice = int(input())

        match choice:
            case 1:
                jug1 = 4
                print("JUG1: ",jug1," JUG2: ", jug2)

            case 2:
                jug2 = 3
                print("JUG1: ",jug1," JUG2: ", jug2)

            case 3:
                while(jug1 >0 and jug2<3):
                    jug1-=1
                    jug2+=1
                print("JUG1: ",jug1," JUG2: ", jug2)
        
            case 4:
                while(jug2 >0 and jug1<4):
                    jug2-=1
                    jug1+=1
                print("JUG1: ",jug1," JUG2: ", jug2)

            case 5:
                jug1 = 0
                print("JUG1: ",jug1," JUG2: ", jug2)

            case 6:
                jug2 = 0
                print("JUG1: ",jug1," JUG2: ", jug2)

```
