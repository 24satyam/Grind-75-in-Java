# Day 01 of Leetcode 75 challenge  
## _Today I have solved Two Sum problem_

[Two Sum](https://leetcode.com/problems/two-sum/description/)

```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        
        HashMap<Integer, Integer> map = new HashMap<>();
        
        for (int i = 0; i < nums.length; i++) {
            int diff = target - nums[i];
            
            if (map.containsKey(diff)) {
                return new int[]{map.get(diff), i};
            }
            
            map.put(nums[i], i);
        }
        
        return new int[]{-1, -1};
    }



 }

```
### Problem Intuition
- It can be solved in O(n*2) by traaversiong the array twice and checking if (a[i]+a[j] == target)
- But it could be done in linear time using HashMap collection in java .
- Using this we will store (value , index ) of each element and see if ( target - curent elemnt ) value exist in the hashmap.    
- If it exist then return index of curent elemnt and found elemnt else store that (current elment , index) and repeat
  
 
