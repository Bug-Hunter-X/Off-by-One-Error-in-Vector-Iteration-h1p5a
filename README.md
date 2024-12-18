# Off-by-One Error in Vector Iteration

This repository demonstrates a common off-by-one error in C++ when iterating through a `std::vector` using a `for` loop.  The error arises from incorrectly accessing an element beyond the valid index range of the vector, leading to undefined behavior.

The `bug.cpp` file contains the erroneous code, while `bugSolution.cpp` provides a corrected version.

## Bug Description

The bug lies in the loop condition `i <= vec.size()`.  Vectors are zero-indexed, meaning the last valid index is `vec.size() - 1`.  Using `<=` attempts to access an element beyond the end of the vector, resulting in a potential crash or unpredictable behavior.

## Solution

The corrected code in `bugSolution.cpp` uses the condition `i < vec.size()`, ensuring that the loop iterates only through valid indices.