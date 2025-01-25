# VHDL Integer Overflow Bug

This repository demonstrates a common bug in VHDL code: integer overflow in a counter. The `buggy_counter.vhdl` file contains a counter that uses an integer type without properly handling potential overflow.  The `fixed_counter.vhdl` file provides a corrected version.

## Bug Description
The original code uses a simple `if` statement to check if the counter has reached its maximum value (15). However, if there's an unexpected event causing `internal_count` to increment beyond its defined range, there will be an integer overflow. This can lead to unpredictable behavior or a simulation failure.

## Solution
The corrected version in `fixed_counter.vhdl` uses a more robust approach which ensures the internal counter never exceeds the intended range. This solution enhances the reliability of the counter.

## How to use
1. Clone the repository.
2. Simulate both `buggy_counter.vhdl` and `fixed_counter.vhdl` using your preferred VHDL simulator (e.g., ModelSim, GHDL, Vivado).
3. Observe the different behavior and see how the corrected version avoids the overflow error.
