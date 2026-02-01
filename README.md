# MFP-Compiler
A real programming language compiler built with C and LLVM 21 for sys

Project Summary: A system-level language designed for Kernel development using LLVM 21 JIT compilation.
1. Arithmetic & Logic Operations (Rules 1-30)
Rule 1-10: Basic Math (+, -, *, /) – Direct JIT execution on hardware.
Rule 11-20: Comparisons (>, <, ==, !=) – Returns boolean status for kernel branching.
Rule 21-30: Bitwise Ops (&, |, ^, <<, >>) – Critical for hardware register masking and flag setting.
2. Memory & Pointer Management (Rules 31-60)
Rule 31: alloc [size] – Reserves raw bytes in system memory.
Rule 32: poke [addr] [val] – Writes a value directly to a physical/virtual memory address.
Rule 33: peek [addr] – Reads and returns the value stored at a specific memory location.
Rule 34-60: Pointer Arithmetic – Calculations to navigate through memory blocks and arrays.
3. Variables & Symbol Table (Rules 61-80)
Rule 61: set [name] = [val] – Defines a persistent integer variable in the LLVM context.
Rule 62-80: Variable scope and cross-reference rules for multi-line script execution.
4. System Flow & Hardware Control (Rules 81-100)
Rule 81: out [expression] – The primary command to trigger LLVM's execution engine.
Rule 82: exit – Safely destroys the JIT engine and releases hardware resources.
Rule 83-100: Kernel Extensions – Placeholder rules for Interrupt calls (INT), GDT loading, and VGA memory mapping (0xA0000).
