# Unexpected NaN Handling in JavaScript Addition

This repository demonstrates a common yet subtle bug in JavaScript related to handling `NaN` (Not a Number) values in arithmetic operations.  The provided `bug.js` file contains a function that intends to handle `null` values gracefully but fails to explicitly address `NaN`, leading to unexpected results.

The `bugSolution.js` file provides a corrected version of the function, showcasing how to properly account for `NaN` inputs to avoid unexpected behavior.

## Bug Description

The original `foo` function correctly handles `null` values by returning 0. However, when either `a` or `b` is `NaN`, the addition operation propagates `NaN` throughout the calculation, leading to an incorrect result.  This can be difficult to debug, especially when `NaN` values arise from previous calculations within a larger application.

## Solution

The solution demonstrates a more robust approach by explicitly checking for `isNaN` before proceeding with the addition operation. If either input is `NaN`, the function now returns 0 (or another suitable default value). This ensures consistent and predictable behavior in all cases, including those involving `NaN`.

This example highlights the importance of considering `NaN` values in your JavaScript code, particularly when dealing with user inputs or external data sources where invalid numerical data might be introduced.