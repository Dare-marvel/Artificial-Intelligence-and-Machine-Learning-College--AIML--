### Code
```py
print("-------------------------------------------Missionary & Cannibal Problem---------------------------------------")

rm = 3
rc = 3
lm = 0
lc = 0
um = 0
uc = 0

while True:
    if lm == 3 and lc == 3:
        print("Congratulations, you won!!!")
        break
    else:
        um = int(input("Enter the number of missionaries traveling from right to left: "))
        uc = int(input("Enter the number of cannibals traveling from right to left: "))
        
        if (um + uc) > 2 or (um + uc) <= 0:
            print("Boat can contain maximum 2 members and minimum 1 member. Boat cannot be empty")
            continue
            
        elif (rm - um < 0):
            print("There are less number of missionaries on the right than entered")
            continue

        elif (rc - uc < 0):
            print("There are less number of cannibals on the right than entered")
            continue

        elif (um == 0 and uc == 0):
            print("Boat must contain atleast 1 missionary or cannibal")
            continue

        elif (um < 0 or uc < 0):
            print("Negative numbers not allowed")
            continue
    
        rm -= um
        rc -= uc
        lm += um
        lc += uc

        print("Missionaries on right: ",rm)
        print("Cannibals on right: ",rc)

        print("Missionaries on left: ",lm)
        print("Cannibals on left: ",lc)
        
        if (lm > 0 and lm < lc) or (rm > 0 and rm < rc):
            print("Cannibals ate missionaries. You lost")
            break

        if lm == 3 and lc == 3:
            print("-------------------------------------------Congratulations, you won---------------------------------------")
            break
        
        um = int(input("Enter the number of missionaries traveling from left to right: "))
        uc = int(input("Enter the number of cannibals traveling from left to right: "))
        
        if (um + uc) > 2 or (um + uc) <= 0:
            print("Boat can contain maximum 2 members and minimum 1 member. Boat cannot be empty")
            continue
            
        elif (lm - um < 0):
            print("There are less number of missionaries on the right than entered")
            continue

        elif (lc - uc < 0):
            print("There are less number of cannibals on the right than entered")
            continue

        elif (um == 0 and uc == 0):
            print("Boat must contain atleast 1 missionary or cannibal")
            continue

        elif (um < 0 or uc < 0):
            print("Negative numbers not allowed")
            continue
        
        rm += um
        rc += uc
        lm -= um
        lc -= uc

        print("Missionaries on right: ",rm)
        print("Cannibals on right: ",rc)

        print("Missionaries on left: ",lm)
        print("Cannibals on left: ",lc)
        
        if (rm > 0 and rc > rm) or (lm > 0 and lc >  lm):
            print("Cannibals ate missionaries. You lost")
            break
```
