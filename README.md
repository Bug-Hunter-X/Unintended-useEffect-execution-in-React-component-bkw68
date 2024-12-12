# Unintended useEffect Execution in React

This repository demonstrates a common React bug involving the `useEffect` hook.  The provided `MyComponent` exhibits an infinite render loop because the `useEffect` hook lacks a dependency array. This causes the effect to run after every render, triggering a continuous update cycle.

The solution showcases how to correctly use the dependency array to control when the effect runs.

## Bug
The `bug.js` file contains the problematic code.  The `useEffect` hook, without a dependency array, triggers every time the component re-renders, creating the infinite loop.  This results in excessive console logs and potentially performance issues in more complex scenarios. 

## Solution
The `bugSolution.js` file presents the corrected code. The dependency array `[count]` ensures the effect only runs when the `count` value changes. This resolves the infinite render loop and provides expected behavior.
