# USCC (University Simple C Compiler) - LLVM Optimizations

This project builds upon the USCC framework, a working compiler for a C language subset (USC). The compiler leverages the **LLVM framework** as its core code generation engine.

## Contributions: Compiler Optimization Passes

As part of this project, I designed and implemented several key intermediate representation (IR) optimization passes to enhance code execution efficiency, memory usage, and control flow. My core contributions include:

* **Dataflow Analysis & SSA Construction:**
  * **Static Single Assignment (SSA):** Implemented SSA construction algorithms and removed redundant Phi nodes to streamline IR for subsequent optimizations.
  * **Liveness & Available Expressions Analysis:** Designed dataflow analyses to track variable lifetimes and previously computed expressions.
* **Redundancy Elimination:**
  * **Dead Code Elimination (DCE):** Analyzed the control flow graph to remove redundant computations, unused memory allocations, and dead instructions.
  * **Common Subexpression Elimination (CSE):** Systematically eliminated redundant instructions to reduce computational overhead.
  * **Copy Propagation:** Optimized variable assignments to minimize unnecessary data copying.
* **Control Flow & Loop Optimizations:**
  * **Constant Branch Folding & Dead Block Elimination:** Converted conditional branches with constant conditions into unconditional jumps and pruned unreachable basic blocks.
  * **Speculative LICM:** Implemented Natural Loop identification and Speculative Loop Invariant Code Motion (SpecLICM) to pull invariant code out of loops.
* **Backend & Profiling:**
  * **Edge Profiling:** Analyzed branch probabilities to guide optimizations.
  * **Register Allocation:** Developed custom register allocation strategies (Profile Split, GC) to optimize hardware register usage.

## Building & Testing

To compile the project and run the optimization test suites:
```bash
cd uscc
make clean && make
cd tests
./run_all_tests.sh
```

## License

* **Author:** Marc Lin ([marc1210899@gmail.com](marc1210899@gmail.com), [lin2315@purdue.edu](lin2315@purdue.edu))
* **Base Framework Credits:** Starting code by Sanjay Madhav ([madhav@usc.edu](madhav@usc.edu)). Makefiles and initial concepts by Dr. Changhee Jung (Purdue University).


