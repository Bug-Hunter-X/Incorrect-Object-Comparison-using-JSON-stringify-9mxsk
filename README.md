# Incorrect Object Comparison in TypeScript

This repository demonstrates a common, yet subtle, bug in TypeScript related to comparing objects using `JSON.stringify`.  The `compareObjects` function provides an example of this flawed approach and its limitations.  The solution offers a more robust method for comparing objects, addressing the shortcomings of the initial implementation.

## Bug
The `bug.ts` file contains a function that attempts to compare two objects using `JSON.stringify`. This method is unreliable because it's sensitive to property order and cannot handle functions, dates, or circular references correctly.

## Solution
The `bugSolution.ts` file presents a more robust solution that recursively compares objects, accounting for different property orders and handling various data types more reliably. This avoids the issues presented by using `JSON.stringify` directly.