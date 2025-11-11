nlist = [3, 7, 12, 18, 24, 29, 35, 41, 47, 53, 58, 64, 70]
comparisons = 0
found = False
search_term = int(input("Enter an integer number: "))

# First and last pointers
first = 0
last = len(nlist) - 1

while found == False and last >= first:
    mid = (first + last) // 2
    comparisons += 1

    if search_term == nlist[mid]:
        found = True
        print(f"Found data at position {mid} used {comparisons} comparisons to find it")  # Print the position
        break
    else:
        if search_term > nlist[mid]:
            first = mid + 1
          
        elif search_term < nlist[mid]:
            last = mid - 1
else:
    print("Not Found data item")
