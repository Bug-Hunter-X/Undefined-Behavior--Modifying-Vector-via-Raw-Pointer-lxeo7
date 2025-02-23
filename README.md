# Rust Undefined Behavior Example

This repository demonstrates a common source of undefined behavior in Rust: modifying a vector through a raw pointer after the vector's capacity might have changed.  The example shows how to reproduce the issue and a safer alternative.

## The Problem

Directly manipulating memory with raw pointers in Rust requires extreme caution.  If the underlying data structure changes (e.g., vector reallocation), the pointer becomes invalid, leading to unpredictable results (crashes, data corruption, etc.).

## Solution

The solution avoids raw pointers and utilizes Rust's safe memory management features.