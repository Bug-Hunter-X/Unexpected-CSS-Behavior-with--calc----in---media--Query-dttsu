# Unexpected CSS Behavior with `calc()` in `@media` Query

This repository demonstrates a subtle but potentially problematic issue involving the use of the `calc()` function within CSS `@media` queries. The problem arises from an incorrect unit handling within the `calc()` expression. 

The `bug.css` file contains the erroneous code, while `bugSolution.css` provides the corrected version.  The core issue lies in trying to directly subtract pixels from `vw` units without proper unit consistency within the `calc()` function.

## How to Reproduce

1. Open `bug.css` and note the incorrect `@media` query using `calc()`. 
2. Observe that the media query is likely to fail or behave inconsistently across different viewport sizes.
3. Compare with the corrected code in `bugSolution.css`. 
4. Test the corrected code to see its consistent behavior.  The solution ensures proper unit handling within the `calc()` function.

## Solution

The solution in `bugSolution.css` addresses the unit inconsistency by ensuring that a consistent unit type is used throughout the `calc()` expression.  This guarantees consistent behavior across different viewport sizes.
