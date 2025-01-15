# Unsafe Rust: Vector Raw Pointer Manipulation

This repository demonstrates a potential issue with directly manipulating a Rust vector's raw pointer using `as_mut_ptr()`.  Directly modifying the data through the raw pointer can lead to memory unsafety and unexpected program behavior, particularly if not done with extreme caution.

The `bug.rs` file contains the problematic code that directly modifies the vector's internal data via its raw pointer.  This bypasses Rust's ownership and borrowing system, leading to potential memory corruption and undefined behavior. 

The `bugSolution.rs` file provides a safe alternative, leveraging Rust's safe abstractions to avoid memory safety issues.