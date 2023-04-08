# Selection Sort
### What is the Selection Sort? 
This sorting method utilizes in-place comparison and has a time complexity of O(n<sup>2</sup>), making it inefficient for sorting large lists. <br>
The Selection sort algorithm works by dividing a list into two parts: 
the sorted part, located at the left end, and the unsorted part, located at the right end. 
Initially, the sorted part is empty and the unsorted part is the entire list. 
The algorithm selects the smallest element from the unsorted part and replaces it with the first element of the sorted part. 
This process is repeated until the entire list is sorted.
<br>

### Sort this series according to selection sort algorithm. -> *[22,27,16,2,18,6]* 
1. After examining all other numbers on the list, the smallest number, which is currently 2, is selected and replaced with 22.
   - [**2**,27,16,22,18,6] **-> n comparisons** 

2. In the next step, we select the smallest number from the unsorted section, which is currently 6, and replace it with 27.
   - [2,**6**,16,22,18,27] **-> (n-1) comparisons** 

3. In step 3, we search for the smallest number in the unsorted section. However, since the number is already at the top of the unsorted section, there is no need to make any changes to the list. This number is then included in the sorted portion.
   - [2,6,**16**,22,18,27] **-> (n-2) comparisons** 

4. In step 4, the smallest number is 18, so we replace it with 22.
   - [2,6,16,**18**,22,27] **-> (n-3) comparisons** 

5. Next, we search for the smallest number again, which is 22, but we do not move it since it is already in the correct position.
   - [2,6,16,18,**22**,27] **-> (n-4) comparisons** 

6. Finally, we arrive at the last number, which is 27. Although its position is already correct, a comparison is still made to confirm this.
   - [2,6,16,18,22,**27**] **-> 1 comparisons** 

**All Comparison = (n-1) + (n-2) + ...  + 1 = n(n-1)/2** <br>
This formula is expressed as O(n<sup>2</sup>) because as n grows, the number of steps becomes proportional to n<sup>2</sup>.


### The first 4 steps according to Selection Sort of the series -> [7,3,5,8,2,9,4,15,6] 
* [**2**,3,5,8,7,9,4,15,6]
* [2,**3**,5,8,7,9,4,15,6] 
* [2,3,**4**,8,7,9,5,15,6]
* [2,3,4,**5**,7,9,8,15,6]