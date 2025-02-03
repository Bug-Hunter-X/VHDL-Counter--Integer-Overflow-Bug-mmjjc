# VHDL Counter with Integer Overflow Bug

This repository demonstrates a common VHDL coding error involving potential integer overflow in a simple counter.  The `buggy_counter.vhdl` file contains the buggy code.  The `fixed_counter.vhdl` file provides a corrected version.

## Bug Description

The original counter increments without properly handling the upper bound of the `integer` range. This leads to an incorrect value after the counter reaches its maximum.  The fix involves ensuring that the counter properly resets to 0 upon reaching the upper limit, preventing overflow.

## How to reproduce the bug

1. Simulate `buggy_counter.vhdl`. 
2. Observe the `count` output after it reaches 15. You'll likely see unexpected values.

## Bug Fix

The corrected version in `fixed_counter.vhdl` addresses the overflow by explicitly resetting the counter when it reaches the maximum value (15).

## Lessons Learned

- Always check for potential integer overflow in counters and other arithmetic operations.
- Employ robust error handling to avoid unexpected behavior.
- Use appropriate data types and ranges to prevent out-of-bounds issues.