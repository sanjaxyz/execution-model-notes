# Execution Order and Call Stack

This document explains how smart contract functions execute during a transaction.

## Sequential Execution

Within a transaction, operations execute sequentially.
Each instruction runs in order, one after another.

Execution does not occur in parallel.

## Function Calls

When a function calls another function:
1. The current execution pauses.
2. The called function begins executing.
3. Once the called function completes, control returns to the original function.

This behavior forms a call stack.

## Call Stack Concept

The call stack represents the order of function execution.
Each new function call is placed on top of the stack.
When a function finishes, it is removed from the stack, and execution continues from the previous level.

## State Updates During Execution

State changes occur during execution.
However, those changes only become final if the entire transaction completes successfully.

If execution fails at any level, the entire call stack is reverted.
