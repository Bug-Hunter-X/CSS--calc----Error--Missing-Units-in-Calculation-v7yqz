# CSS `calc()` Error: Missing Units

This repository demonstrates a common, yet subtle, error when using the `calc()` function in CSS.  Failing to include units in all parts of the calculation can lead to unexpected behavior or errors in certain browsers.

## The Problem

The `calc()` function allows for dynamic calculation of CSS values. However, if you omit units from a number within the calculation, some browsers might not handle it correctly. For instance:

```css
/* Incorrect: Missing unit in '10' */
.element { width: calc(50% - 10); }
```

This can lead to unpredictable results.  The browser may interpret the unitless number incorrectly or throw an error.

## The Solution

The solution is straightforward: always ensure every value within `calc()` has a unit.  Here's the correct version:

```css
/* Correct: Includes unit 'px' */
.element { width: calc(50% - 10px); }
```

This ensures consistent and expected behavior across different browsers.

## Files

* `bug.css`: Contains the incorrect CSS code demonstrating the bug.
* `bugSolution.css`: Contains the corrected CSS code with the issue resolved.