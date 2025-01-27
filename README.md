# React useEffect Infinite Loop

This repository demonstrates a common React bug involving an infinite loop caused by incorrectly updating state within a useEffect hook.

## Problem:
The `useEffect` hook, when used with an empty dependency array (`[]`), is intended to run only once after the component mounts. However, if the effect updates the state in a way that triggers another render, it results in an infinite loop. The code in `bug.js` illustrates this problem.

## Solution:
The solution provided in `bugSolution.js` demonstrates how to resolve this issue. Instead of directly updating the state, use functional updates to ensure the effect runs only once without causing an infinite loop.