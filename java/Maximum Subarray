# Intuition
<!-- Describe your first thoughts on how to solve this problem. -->

# Approach
<!-- Describe your approach to solving the problem. -->

# Complexity
- Time complexity:
<!-- Add your time complexity here, e.g. $$O(n)$$ -->

- Space complexity:
<!-- Add your space complexity here, e.g. $$O(n)$$ -->

# Code
```java []
class Solution {
    public int maxSubArray(int[] nums) {
        return maxSubArrayMyAlgo(nums);
    }

    private int maxSubArrayMyAlgo(int[] nums) {
        int maxSum = Integer.MIN_VALUE;
        int currSum = 0;

        for (int n: nums) {
            currSum += n;
            if (currSum > maxSum) {
                maxSum = currSum;
            }

            if (currSum < 0) {
                currSum = 0;
            }
        }
        return maxSum;
    }


    private int maxSubArrayKadaneAlgo(int[] nums) {
        int res = nums[0];
  
        for (int i = 0; i < nums.length; i++) {
            int currSum = 0;
            for (int j = i; j < nums.length; j++) {
                currSum = currSum + nums[j];
                if (currSum > res) {
                    res = currSum;
                }
            }
        }
        return res;
    }
}
```
