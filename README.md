# Go Race Condition Example

This repository demonstrates a common race condition in Go when multiple goroutines access and modify a shared variable concurrently without proper synchronization.

## Bug Description
The `bug.go` file contains a program that launches 1000 goroutines, each incrementing a shared `count` variable.  Because there's no synchronization, the final value of `count` will likely be less than 1000 due to race conditions.

## Solution
The `bugSolution.go` file demonstrates how to fix this race condition using a `sync.Mutex` to protect the `count` variable.