# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug is caused by an incorrect dependency array, resulting in an infinite loop of re-renders.

## Bug Description
The `MyComponent` component uses `useEffect` to log the current count to the console after every render.  However, the `count` variable is not included in the dependency array. This means that the effect runs on every render, changing the count, and triggering another render, leading to an infinite loop.

## Solution
The solution involves adding `count` to the dependency array of the `useEffect` hook. This ensures that the effect only runs when the value of `count` changes.