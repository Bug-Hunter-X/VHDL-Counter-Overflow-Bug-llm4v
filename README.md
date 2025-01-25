# VHDL Counter Overflow Bug
This repository demonstrates a common VHDL coding error involving potential integer overflow in a counter and provides a corrected version.

## Bug Description
The original `buggy_counter.vhdl` code implements a counter that increments on each rising clock edge. However, it lacks proper handling of the upper limit, potentially leading to unexpected behavior if the counter exceeds its defined range (0 to 15).

## Solution
The `fixed_counter.vhdl` file presents a corrected version, using a `mod` operator to wrap around safely when the counter reaches its maximum value. This prevents unexpected overflow and maintains consistent behavior.

## How to reproduce the bug
Compile and simulate the buggy counter. Observe that after it reaches 15, it will wrap around incorrectly, leading to unexpected behavior. This may not be immediately apparent in smaller simulations.

## How to use the solution
Replace the buggy counter with the fixed counter in your VHDL design. This will ensure correct operation and prevent any potential overflow issues.
