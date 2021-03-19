# Sorting Algorithms

## Merge Sort
- Recursive
- Divide and Conquer
- Efficient for _large_ data sets
  - Not so much for _smaller_ data sets
- log(n) merge steps
- does _n_ work for each merge step since it must look at every item
- Overall, O(n log(n))
- Space Complexity of O(n)
```python

# MERGE SORT CODE IN PYTHON
def merge(arr, left, middle, right): 
    n1 = middle - left + 1
    n2 = right- middle 
  
    left_arr = [0] * (n1) 
    right_arr = [0] * (n2) 
  
    for i in range(0 , n1): 
        left_arr[i] = arr[left + i] 
  
    for j in range(0 , n2): 
        right_arr[j] = arr[middle + 1 + j] 
  
    i = 0
    j = 0
    k = left
  
    while i < n1 and j < n2 : 
        if left_arr[i] <= right_arr[j]: 
            arr[k] = left_arr[i] 
            i += 1
        else: 
            arr[k] = right_arr[j] 
            j += 1
        k += 1
  
    while i < n1: 
        arr[k] = L[i] 
        i += 1
        k += 1

    while j < n2: 
        arr[k] = R[j] 
        j += 1
        k += 1
  
def mergeSort(arr,left,right): 
    if left < right: 
        middle = (left + (right - 1)) //2
        mergeSort(arr, left, middle) 
        mergeSort(arr, middle  + 1, right) 
        merge(arr, left, middle, right) 
```
[Explanation](https://www.youtube.com/watch?v=Nso25TkBsYI)

[code source](https://www.geeksforgeeks.org/merge-sort/) (modified for clarity)

## QuickSort

## TimSort

## HeapSort

## BubbleSort

## InsertionSort

## Selection Sort

## Tree Sort

## Shell Sort

## Bucket Sort

## Radix Sort

## Counting Sort

## Cube Sort
