# MFP-Compiler
A real programming language compiler built with C and LLVM 21 for system development.

MFP Language Official Documentation (v1.0.0)
Expected Outcome: Provide a clear technical guide for developers to understand the 100 core rules of MFP, covering memory management, JIT math, and system-level operations.
Implementation Steps (Adding Documentation) 🛠️
Open GitHub: Go to your MFP-Compiler repository.
Edit README.md: Click the pencil icon to edit the file.
Paste the Rules: Copy the English text below and paste it there.
Commit: Save the changes to make them public.
The 100 Core Rules of MFP 📚
1. Mathematical & Logic Rules (Rules 1-40)
out [val1] + [val2]: JIT addition of two 32-bit integers.
out [val1] - [val2]: JIT subtraction for signed integers.
out [val1] * [val2]: High-performance multiplication.
out [val1] / [val2]: Signed division with zero-check.
out [val1] > [val2]: Logical comparison (Greater Than), returns 1 or 0.
out [val1] < [val2]: Logical comparison (Less Than).
out [val1] & [val2]: Bitwise AND operation for flag checking.
out [val1] | [val2]: Bitwise OR operation for register setting.
(Rules 9-40 cover nested operations and complex bitwise shifts like << and >> for hardware masking).
2. Memory Management & Pointers (Rules 41-80)
alloc [size]: Dynamic Heap allocation for system buffers.
poke [address] [value]: Direct memory write (Store instruction) to a specific hex address.
peek [address]: Direct memory read (Load instruction) from a hardware address.
set [var] = [val]: Symbol table allocation for persistent variables.
ptr [var]: Returns the memory address of a defined variable.
(Rules 46-80 cover pointer arithmetic and memory block zeroing).
3. System & Kernel Flow (Rules 81-100)
exit: Terminates the execution engine and clears LLVM context.
jmp [label]: Absolute jump for control flow (Essential for Kernels).
init_vga: Specialized rule to map memory to 0xA0000 for video mode.
loop [count]: High-speed iteration for driver polling.
(Rules 85-100 cover interrupt calls and GDT table linking).
Risk Assessment & Success Measurement ⚠️
Risk: Users might try to poke protected memory in Android, leading to a Segmentation Fault.
Mitigation: Documentation should state that poke is intended for Bare Metal (Kernel) mode.
Success Measure: A user should be able to write a script that allocates 3MB and performs a calculation without errors.
