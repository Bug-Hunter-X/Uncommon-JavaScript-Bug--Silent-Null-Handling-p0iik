# Uncommon JavaScript Bug: Silent Null Handling

This repository demonstrates a subtle bug in JavaScript related to how null values are handled in a function. The function `foo` adds two numbers, but silently returns 0 if either input is null.  This behavior might be unexpected and could lead to errors that are difficult to track down.

The `bug.js` file shows the buggy code. The `bugSolution.js` demonstrates an improved version with more robust null handling.

## Bug Description:

The `foo` function handles `null` values by returning 0 without any explicit indication of an error. While seemingly simple, this can be problematic. In many scenarios, it's more appropriate to explicitly signal an error condition, or perhaps handle nulls differently depending on the context.

## Solution:

The improved version in `bugSolution.js` throws an error when a null value is encountered, providing clearer indication of the problem. This approach helps to make the error more visible and makes the code easier to debug.  Alternatively, you might want to return `NaN` or a different default value depending on your application's requirements.

## How to Run:

1. Clone this repository.
2. Open `bug.js` and `bugSolution.js` in your preferred JavaScript environment.
3. Run the code and observe the outputs.