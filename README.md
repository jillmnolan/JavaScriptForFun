﻿# Two Number Sum

## Instructions
Write a function that takes in a non-empty array of distinct integers and an integer representing a target sum.  If any two numbers in the input array sum up to the target sum, the function should return them in an array, in any order.  If no two numbers sum up to the target sum, the function should return an empty array.  Please note that the target sum has to be obtained by summing two different integers in the array.  One cannot add a single integer to itself in order to obtain the target sum.  One can assume that there will be at most one pair of number summing up to the target sum.

```javascript
// 0(n^2) time | 0(1) space

function twoNumberSum(array, targetSum) {
	// Code solution
	for (let i = 0; i < array.length - 1; i++) {
		const firstNum = array[i];
		for (let j = i + 1; j < array.length; j++) {
			const secondNum = array[j];
			if (firstNum + secondNum === targetSum) {
				return [firstNum, secondNum];
			}
		}
	}
	return[];
}

// Please do not modify this code snippet
export.twoNumberSum = twoNumberSum;
```
