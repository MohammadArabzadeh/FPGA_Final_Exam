# FPGA_Final_Exam
this is final exam of computer organization laboratory in Electrical Engineering Department  in Iran's University of Science and Technology. January 2025
This VHDL code describes a Counter Module that counts from 0 to 50 in an up/down fashion based on a control signal (key). Here’s a breakdown of its features:

Functionality

Clock Divider

The input clock is divided to generate a 1-second pulse (clk_1s), ensuring the counter updates once per second.
Counting Mechanism

Two BCD counters (count_ones and count_tens) represent the ones and tens places, respectively.
The counter increments (Rotation = '1') or decrements (Rotation = '0') based on the key signal.
The rollover signal ensures that the tens place increments when the ones place transitions from 9 to 0.
Special Conditions

The counter stops at 50 when counting up.
The counter stops at 00 when counting down.

Signals

pr_state_ones, pr_state_tens: Track the current state for ones and tens.
nx_state_ones, nx_state_tens: Determine the next state.
clk_1s: Generated clock pulse (1 Hz).
rollover: Signals when tens should increment.
Possible Improvements
Reset Behavior
Currently, reset initializes states to 0, but additional logic might be needed for synchronous reset.
Clock Edge Detection for key
Currently, key toggles Rotation asynchronously, which may cause glitches.
Would you like modifications to optimize the counter or add testbench code? 🚀
