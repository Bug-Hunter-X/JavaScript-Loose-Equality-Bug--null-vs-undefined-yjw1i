# JavaScript Loose Equality Bug: null vs undefined

This repository demonstrates a subtle bug related to the loose equality operator (==) in JavaScript when comparing null and undefined.  The issue arises from JavaScript's type coercion rules, which can lead to unexpected results if not carefully considered.

## The Bug
The provided `foo` function aims to handle null values, returning 0 if `a` is null, otherwise adding 1 to `a`. However, due to loose equality, `undefined` is also treated as 0, leading to an unexpected result when `undefined` is passed as an argument.

## The Solution
The solution uses strict equality (===) which prevents type coercion, ensuring that only null values are considered.

## How to reproduce:
1. Clone the repository
2. Open `bug.js` and observe the console output.
3. Open `bugSolution.js` to see the corrected implementation. 