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
## i)Use a linear search method to match the item in a list.
```python
''' 
Program for linear search method to match the item in a list
Developed by:MOHAMED FAREED.F
RegisterNumber:22001617
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if array[i]==k:
            return i
    return -1
array = eval(input())
k = eval(input()) 
n=len(array)
array.sort()
result =linearSearch(array,n,k)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)


```
## ii)Find the element in a list using Binary Search(Iterative Method).
```python
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:MOHAMED FAREED.F
RegisterNumber:22001617
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
k=eval(input())
result=binarySearchIter(array,k,0,len(array)-1)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)





```
## iii)Find the element in a list using Binary Search (recursive Method).
```python
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by:Vasanthamukilan.M
RegisterNumber:22001986
'''
def binarySearch(arr, k, low, high):
    if low<=high:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]>k:
            return binarySearch(arr,k,low,mid-1)
        else:
            return binarySearch(arr,k,mid+1,high)
    return -1
array = eval(input())
array.sort()
k = eval(input())
result=binarySearch(array,k,0,len(array)-1)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)




```
## Output
## i)Use a linear search method to match the item in a list.
![Screenshot_20230126_020749](https://user-images.githubusercontent.com/121412904/214791754-28ccb087-9765-4d4b-90ff-4d098e2eeecf.png)
## ii)Find the element in a list using Binary Search(Iterative Method).
![Screenshot_20230126_021316](https://user-images.githubusercontent.com/121412904/214793003-d9b54ba9-9650-4db7-b595-a634720be03b.png)
## iii)Find the element in a list using Binary Search (recursive Method).
![Screenshot_20230126_021833](https://user-images.githubusercontent.com/121412904/214793732-3d62f93c-9e3e-4dae-a3e5-26704d843e77.png)







## Result
Thus the linear search and binary search algorithm is implemented using python programming.
