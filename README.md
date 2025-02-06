# Uncommon CSS `calc()` Issues

This repository demonstrates two uncommon errors related to the CSS `calc()` function: incorrect spacing and inconsistent units.  These issues can be difficult to debug because `calc()` silently ignores invalid expressions without producing any error messages in the browser's developer console.

## Bug 1: Incorrect Spacing in `calc()`
Spaces around the plus or minus operators in `calc()` expressions can cause unexpected behavior.  For example, `width: calc(100% - 10px);` works correctly, but `width: calc(100%  -  10px);` might not.

## Bug 2: Inconsistent Units in `calc()`
Mixing units in `calc()` without proper conversion can also lead to issues. While `height: calc(50% + 10em);` is valid, other inconsistent uses will likely result in incorrect calculations.

## Bug 3: Invalid `calc()` Expressions
If your `calc()` expression contains an invalid expression, the entire property declaration will be ignored without producing an error message, leading to subtle and difficult-to-find bugs.  These situations need careful inspection.

## Solutions
Solutions are shown in `bugSolution.css`.