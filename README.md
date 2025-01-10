# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency in the dependency array.  The bug is explained in detail and a solution is provided.

## Bug Description

The `useEffect` hook is designed to perform side effects after every render. When the dependency array is omitted or incomplete, the effect runs on every render, creating an infinite loop.  The example demonstrates this with a counter that continuously updates, logging to the console and causing performance issues.

## Bug Solution

The solution involves correctly specifying the dependencies within the dependency array.  By including `count` in the array, the effect only runs when the value of `count` changes, preventing the infinite loop.