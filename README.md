# Express.js Route Parameter Error Handling: Non-numeric IDs

This repository demonstrates a common error in Express.js route handling where non-numeric parameters are not properly handled, leading to potential crashes or unexpected behavior.  The `bug.js` file showcases the flawed code, while `bugSolution.js` provides the corrected version with robust error handling.

## Bug Description
The original code attempts to access a user based on an ID passed in the route parameters. However, it doesn't check if the ID is actually a number.  If a non-numeric value is provided, `parseInt` will return `NaN`, resulting in the code failing to find the user and potentially causing errors further down the line.

## Solution
The solution in `bugSolution.js` addresses this issue by adding input validation.  It explicitly checks if the ID is a number using `isNaN`. If the ID is invalid, a proper 400 Bad Request response is sent.