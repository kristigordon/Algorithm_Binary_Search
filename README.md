
![image](https://user-images.githubusercontent.com/66803124/118513589-b927e700-b6e8-11eb-99a9-5617386d6970.png)

# Algorithm_Binary_Search

![image](https://user-images.githubusercontent.com/66803124/118511758-128f1680-b6e7-11eb-9cb8-fbe17e5b5b4e.png)

The best way I have seen a Binary Search Algorithm explained has been in Harvard's CS50 Computer Science course. 

https://www.youtube.com/watch?v=DSffdCT5Cx4

Here, Professor David Malan works his way through this algoritm using a phone book.

One fundemental part of Binary searches is that the list you are iterating through must have already been ordered. That is why the phone book in this example works perfectly. 

Say we are looking for some hot shot in the phone book, let's call her Kristi Gordon. 

We could flip through every single page of the phone book and eventually get to the correct entry, however this is painfully slow. That is where a binary search comes in!

Instead, since our phone book is ordered, we can open it half way and see maybe the M's or N's. We then know that we have passed Gordon so we can tear the phone book in half because we know Gordon isn't in the second half of the book. 

That means we just tore our problem in half, literally! From say 1,000 pages to 500 in this case but this number can be astronomical depending on the circumstance. 

Now, we can If we do this again to our book, we end up at a point in the H's. That just halved our problem again down to 250. We keep iterating through this loop until we have found our target. 

Ok! We've found Kristi Gordon. Looks like she's an experienced Technical Program Manager looking for employment! Let's wrap up this algorithm and give her a call. 

Lastly, this can be done with so much more than a name in a phone book, including numbers. Here is a graphical representation of the above explanation followed by an example solution. 

![image](https://user-images.githubusercontent.com/66803124/118507993-9d6e1200-b6e3-11eb-929d-d5443b7c8fe2.png)

# Coding Question Example: 
```
Given an array of integers nums which is sorted in ascending order, 
and an integer target, write a function to search target in nums. 
If target exists, then return its index. Otherwise, return -1.
```
You must write an algorithm with O(log n) runtime complexity.

Example 1:
```
Input: nums = [-1,0,3,5,9,12], target = 9
Output: 4
Explanation: 9 exists in nums and its index is 4
Example 2:
```
```
Input: nums = [-1,0,3,5,9,12], target = 2
Output: -1
Explanation: 2 does not exist in nums so return -1
```

Constraints:

1 <= nums.length <= 104
-9999 <= nums[i], target <= 9999
All the integers in nums are unique.
nums is sorted in an ascending order.

# Possible Solution

```
    def search(self, nums: List[int], target: int) -> int:
        left, right = 0, len(nums) - 1
        while left <= right:
            pivot = left + (right - left) // 2
            if nums[pivot] == target:
                return pivot
            if target < nums[pivot]:
                right = pivot - 1
            else:
                left = pivot + 1
        return -1
```
