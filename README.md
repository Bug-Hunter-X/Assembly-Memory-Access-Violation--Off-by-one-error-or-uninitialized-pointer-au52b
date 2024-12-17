# Assembly Memory Access Violation Bug Report

This repository demonstrates a common error in assembly programming: a memory access violation caused by an incorrect address calculation.  The bug can manifest in several ways, including segmentation faults, unexpected program termination, and potentially security vulnerabilities if exploited maliciously. The example shows how a simple off-by-one error or uninitialized pointer can lead to memory access issues.

## Bug Description
The `bug.asm` file contains assembly code with a flaw in memory access. The `mov` instruction calculates an address dynamically and then reads data from that address. However, the calculation can easily result in an invalid memory address, especially if variables are uninitialized or if there's an off-by-one error in indexing. This will cause a segmentation fault or other unpredictable behavior.

## Solution
The `bugSolution.asm` file offers a corrected version of the code. It addresses the error by ensuring the values used in the address calculation are valid and that the index is correctly calculated.