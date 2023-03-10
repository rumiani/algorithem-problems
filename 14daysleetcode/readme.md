
# 14 Days Algorithem-Problems sloving challenge using TypeScript

Source: [leetcode.com](https://leetcode.com)

## 1- Binary Search

Given an array of integers `nums` which is sorted in ascending order, and an integer `target`, write a function to search `target` in `nums`. If target exists, then return its index. Otherwise, return `-1`.
You must write an algorithm with O(log n) runtime complexity.

**Example:**

- `Input: nums = [-1,0,3,5,9,12], target = 9
Output: 4
Explanation: 9 exists in nums and its index is 4`

- `Input: nums = [-1,0,3,5,9,12], target = 2
Output: -1
Explanation: 2 does not exist in nums so return -1`

**Solution:**

```typescript
function search(nums: number[], target: number): number {
    return nums.indexOf(target);
};
```

[Test out the solution here](https://leetcode.com/problems/binary-search/?envType=study-plan&id=algorithm-i)
