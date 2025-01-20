Overview

This repository contains a SystemVerilog class-based implementation of a pattern generator that toggles a single bit and a corresponding testbench. The pattern generator alternates the value of a bit and prints its current value with each invocation.

Functional Description

Pattern Generator Class

The pattern_generator class includes:

Data Members:

bit current_value: A single bit that toggles between 0 and 1.

Methods:

new(): Constructor that initializes current_value to 0.

generate_next(): Task to:

Print the current value of current_value.

Toggle current_value to its complement (~current_value).

Execution Flow

The pattern_generator object pg is created using the constructor.

The generate_next task is called 10 times within a repeat loop.

Each invocation:

Prints the current value of the bit.

Toggles the bit for the next state.

The simulation ends with a $finish statement.

Example Output

For 10 iterations, the output will alternate between 0 and 1:
0101010101
