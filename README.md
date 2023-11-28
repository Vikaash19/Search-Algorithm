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
~~~
''' 
Program for linear search method to match the item in a list
Developed by: Vikaash K S
RegisterNumber: 23013426
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i]==k):
            return i
    return -1
    
array = eval(input())
k = eval(input()) 
n=len(array)
array.sort()
result = linearSearch(array,n,k)
print(array)
if(result== -1):
    print("Element not found")
else:
    print("Element found at index: ",result)
~~~
ii)	# Find the element in a list using Binary Search(Iterative Method).
~~~
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: Vikaash K S
RegisterNumber: 23013426
'''
def binarySearchIter(array, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1

array = eval(input())
array.sort()
k = int(input())
low=0
high=len(array)-1
result=binarySearchIter(array, k, low, high)
print(array)
if (result==-1):
    print("Element not found")
else:
    print("Element found at index: ",result)

~~~
iii)	# Find the element in a list using Binary Search (recursive Method).
~~~
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: Vikaash K S
RegisterNumber: 23013426
'''
def BinarySearch(arr, k, low, high):
    if high>=low:
        mid=(high+low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]>k:
            return BinarySearch(arr, k,low,mid-1)
        else:
            return BinarySearch(arr, k, mid+1, high)
    else:
        return -1
arr = eval(input())
arr.sort()
print(arr)
k = eval(input())
low=0
high=len(arr)-1
r=BinarySearch(arr, k, low, high)
if(r==-1):
    print("Element not found")
else:
    print("Element found at index: ",r)
~~~
## Sample Input and Output:
![sample input and output](https://github.com/Vikaash19/Search-Algorithm/assets/148514589/78a13c8b-cff6-4500-a501-b6c3c9f54660)

## Output:
![array linear search](https://github.com/Vikaash19/Search-Algorithm/assets/148514589/aa6c3ab0-d1e7-4f52-8250-41ca3cf32b48)

![array bin iter search](https://github.com/Vikaash19/Search-Algorithm/assets/148514589/70493203-3e7a-42bc-b0aa-62215c7540fd)

![array bin rec search](https://github.com/Vikaash19/Search-Algorithm/assets/148514589/b7c9658e-02dc-461c-bfd2-dce7b1645471)

## Result:
Thus the linear search and binary search algorithm is implemented using python programming.
