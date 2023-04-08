# Merge Sort
### What is the Merge Sort? 
Merge sort is a popular sorting algorithm that works by dividing the input list into smaller lists, sorting them recursively, 
and then merging them back together to produce a sorted list. <br>
It is a "divide and conquer" algorithm that can handle large data sets efficiently, with a time complexity of **O(n log n)**. <br>

### Sort this series according to Merge Sort algorithm. -> *[16,21,11,8,12,22]* 
1. Divide the list into two halves recursively until each sublist contains only one element.
   - Divide the list into two halves:
     - [16,21,11,8,12,22] -> [16,21,11] - [8,12,22]

   - Divide the left and right halves recursively:
     - [16,21,11] -> [16] - [21,11]
     - [8,12,22] -> [8] - [12,22]

   - It is divided until it contains only one item.:
     - [21,11] -> [21] - [11]
     - [12,22] -> [12] - [22]
   - **[16] - [21] - [11] - [8] - [12] - [22]**


2. Sort each sublist using the same merge sort algorithm recursively until each sublist is sorted.
   - Sort each half:
     - [21] - [11] -> [11,21]
     - [12] - [22] -> [12,22]
   - Sort the left and right halves recursively:
     - [16] - [11,21] -> [11,16,21]
     - [8] - [12,22] -> [8,12,22]
   - **[11,16,21] - [8,12,22]**

3. Merge the two sorted sublists back together to form a single sorted list.
   - Merge the two halves:
     - **[8, 11, 12, 16, 21, 22]**