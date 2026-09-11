# Test Command

this memo records how to run unit test and end-to-end test.
make sure to compile before testing.

```
cd uscc
make
```

## All test

```
cd uscc/tests
./run_all_tests.sh
```

## PA1

```
cd uscc/tests/pa1
python3 testPeeling.py
python3 testLifting.py
python3 testInstcombine.py
```

Contribution:

- parse/ASTEmit.cpp
- parse/ASTtoCode.cpp
- opt/InstCombine.cpp 

## PA2

```
cd uscc/tests/pa2
python3 testNaturalLoop.py
python3 testEdgeProfiling.py
```

Contribution:

- opt/NaturalLoopInfo.cpp
- opt/EdgeProfiling.cpp
- opt/EdgeProfilingOpt.cpp


## PA3

```
cd uscc/tests/pa3
python3 testLiveness.py
python3 testAE.py
```

Contribution:

- opt/AvailableExpressions.cpp
- opt/Liveness.cpp
- opt/DCE.cpp
- opt/CSE.cpp


## PA4

```
cd uscc/tests/pa4
python3 testCopyProp.py
python3 testSSA.py
python3 testPhi.py
```

Contribution:

- opt/SSABuilder.cpp
- parse/Symbols.cpp
- parse/ASTEmit.cpp
- opt/RedundantPhi.cpp
- opt/CopyPropagation.cpp


## PA5

```
cd uscc/tests/pa5
python3 testConstantDeadBlock.py
python3 testSpecLICM.py
```

Contribution:

- opt/ConstantBranch.cpp
- opt/DeadBlocks.cpp
- opt/SpecLICM.cpp


## PA6

```
cd uscc/tests/pa6
python3 testRegAlloc.py
```

Contribution:

- opt/RegAllocProfileSplit.cpp
- opt/RegAllocGC.cpp