# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug is caused by a missing dependency in the `useEffect` hook, leading to an infinite rendering loop.

## Bug Description
The `useEffect` hook in `bug.js` is designed to log the current count to the console. However, because it lacks the `count` variable as a dependency, the effect runs on every render, causing the `count` to update, triggering another render, leading to an infinite loop and potential crashes.

## Solution
The `bugSolution.js` file demonstrates the corrected code. By adding `count` as a dependency, the effect only runs when the `count` variable changes, fixing the infinite loop issue. This is a crucial concept for understanding and preventing performance issues in React applications.