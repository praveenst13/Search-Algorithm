# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
Developed by:PRAVEEN S
RegisterNumber: 22009017
def linear(array,n,k):
    for i in range(0,n):
        if(array[i] == k):
            return i
    return -1
array =eval(input())
k=eval(input())
n = len(array)
array.sort()
result = linear(array,n,k)
if(result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
Developed by:PRAVEEN S
RegisterNumber: 22009017
def binarySearchIter(array, k, low, high):
    # Write your code here to find the middle value and check if the desired item is above or below the middle value
    while low <= high :
        mid = low +(high-low)//2
        if array[mid] == k:
            return mid
        elif array[mid] < k:
            low = mid+1
        else:
            high = mid - 1
    return -1
array = eval(input())
# sort the array
k = eval(input()) #k-item to be searched
array.sort()
result = binarySearchIter(array, k,0, len(array)-1)
if (result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)

``` 
iii)	# Find the element in a list using Binary Search (recursive Method).
 ```
def binarySearchIter(array, k, low, high):
    # Write your code here to find the middle value and check if the desired item is above or below the middle value
    while low <= high :
        mid = low +(high-low)//2
        if array[mid] == k:
            return mid
        elif array[mid] < k:
            low = mid+1
        else:
            high = mid - 1
    return -1
array = eval(input())
k = eval(input()) #k-item to be searched
array.sort()
result = binarySearchIter(array, k,0, len(array)-1)
if (result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
```
## Sample Input and Output
i[out](input.png)
## Output:
![img](l1.png)
i[img](b1.png)
![img](b2.png)
## Result
Thus the linear search and binary search algorithm is implemented using python programming.
