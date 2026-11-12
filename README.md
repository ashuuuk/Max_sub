# Maximum Subarray Visualizer

An interactive algorithm visualizer for **LeetCode 53 – Maximum Subarray**, built to demonstrate how **Kadane's Algorithm** finds the maximum sum of a contiguous subarray through step-by-step execution.

The project allows users to enter their own arrays, observe every iteration, understand the algorithm's decisions, and see the final maximum subarray sum.

## Overview

Given an integer array `nums`, find the contiguous subarray (containing at least one number) that has the largest sum, and return its sum.

**Example:**

```text
Input:
nums = [-2, 1, -3, 4, -1, 2, 1, -5, 4]

Output:
6

Maximum Sum Subarray:
[4, -1, 2, 1]
```

## Features

- **Custom Array Input:** Specify the array size and enter your own integer elements.
- **Step-by-Step Visualization:** Follow Kadane's Algorithm as it processes each element.
- **Dynamic Array Highlighting:** Visually distinguish the current subarray from the best subarray found so far.
- **Iteration History:** Track the index, current element, decision, current sum, and maximum sum.
- **Step Navigation:** Move forward and backward through individual algorithm iterations.
- **Final Result:** Displays the maximum sum along with the corresponding subarray and its indices.
- **Preset Test Cases:** Quickly test classic, all-negative, and all-positive arrays.
- **Responsive Interface:** Works on desktop, tablet, and mobile devices.

## Understanding Kadane's Algorithm

Kadane's Algorithm solves the Maximum Subarray problem using Dynamic Programming.

At each index, we decide whether to:

1. Extend the existing subarray by including the current element.
2. Start a new subarray from the current element.

We maintain two variables:

- `currentSum`: The maximum sum of a subarray ending at the current position.
- `maxSum`: The maximum subarray sum found so far.

### Algorithm

```text
currentSum = nums[0]
maxSum = nums[0]

for i = 1 to n-1:

    currentSum = max(nums[i],
                     currentSum + nums[i])

    maxSum = max(maxSum, currentSum
