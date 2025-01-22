# JavaScript Closure Gotcha in setTimeout Loop

This repository demonstrates a common error in JavaScript involving closures and the `setTimeout` function within a loop.  The incorrect code results in unexpected behavior due to how closures capture variables.

## Problem

The `bug.js` file contains a function that uses a `for` loop and `setTimeout`. The intention is to log the values 0 through 9 with a one-second delay between each log.  However, due to a closure issue, it incorrectly logs 10 ten times.

## Solution

The `bugSolution.js` file provides a corrected version.  It uses an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop, ensuring that the correct value of `i` is captured for each `setTimeout` call.