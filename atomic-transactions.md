# Atomic Transactions

This document explains the concept of atomic execution in blockchain systems.

## What Does "Atomic" Mean?

In blockchain systems, a transaction is atomic.  
This means that all operations within the transaction either succeed together or fail together.

Partial execution does not persist.

## High-Level Behavior

1. A transaction is submitted to the network.
2. The transaction executes step by step.
3. If every step completes successfully, the state changes are applied.
4. If any step fails, all intermediate state changes are reverted.

## State Reversion

If execution fails at any point:
- The blockchain state returns to what it was before the transaction began.
- No partial updates remain.
- No intermediate balances or contract changes persist.

## Result

Atomicity ensures that blockchain transactions maintain consistent state, even when execution fails.
