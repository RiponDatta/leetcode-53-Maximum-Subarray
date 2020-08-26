# leetcode 53 - Maximum Subarray

## Greedy Approach
## C#
```C#
public int MaxSubArray(int[] nums)
{
    int currSum = nums[0],
        maxSum = nums[0];
    for (int i = 1; i < nums.Length; i++)
    {
        currSum = Math.Max(nums[i], currSum + nums[i]);
        maxSum = Math.Max(maxSum, currSum);
    }
    return maxSum;
}
```

#### Complexity Analysis

* Time Complexity: O(N)
* Space Complexity: O(1)
