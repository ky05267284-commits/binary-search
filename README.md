# binary-search
nlist = [2, 3, 5, 6, 7, 12, 90, 99, 100, 120]

found=False
search_term = 100

#first and lst pointers
first = 0
last = len(nlist) - 1

while (found == False and last >= first):

mid = (first + last) //2

if (search_term == nlist[mid]):
    found = True
    break

else:

    if (search_term > nlist[mid]):

        first = mid + 1

    elif (search_term < nlist[mid]):

        last = mid - 1
if(found == True):
print("Found data item")
else:
print("Not Found data item")
