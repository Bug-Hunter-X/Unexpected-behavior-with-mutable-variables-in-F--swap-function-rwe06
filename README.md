# F# Mutable Variable Swap Bug

This example demonstrates a common issue when working with mutable variables in F#. The `swap` function aims to exchange the values of two mutable variables, but it doesn't work as intended because of a misunderstanding of how F#'s mutable variable assignment interacts with function parameters.  The original code attempts an in-place swap, but fails to correctly modify the original variables passed to the function.

## Bug Details

The `swap` function is passed copies of the values of `x` and `y`, so modifying those copies within the function doesn't change the original variables. The variables passed to the function are treated as local variables and the changes are not reflected in the original variables outside of the function scope. 