# JavaScript Loose Comparison Bug

This repository demonstrates a common error in JavaScript related to loose comparison (==) resulting in unexpected behavior.  The bug involves comparing numbers and strings without strict type checking, leading to incorrect boolean evaluation.

## Bug Description
The `foo` function uses loose comparison (`==`) to check if two arguments match specific values. However, when comparing a number (1) with a string ("2"), the loose comparison yields `false`, even though one might expect `true` due to the values being numerically equivalent. This is because loose comparison doesn't perform type coercion in this specific case, leading to an inaccurate result.

## Solution
The solution involves switching to strict comparison (`===`) to ensure type and value equality. Strict comparison avoids type coercion, leading to more predictable and reliable results.

## How to reproduce the bug
1. Clone this repository
2. Run `bug.js` using Node.js or a similar JavaScript runtime
3. Observe the unexpected output for `foo(1,"2")`.