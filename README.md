# React useEffect Hook Memory Leak

This repository demonstrates a common error in React applications involving the `useEffect` hook: forgetting to include a cleanup function in the returned value, leading to memory leaks. The example showcases the problem, along with a corrected version.

## Bug Description

The `useEffect` hook without a return statement causes a memory leak because the function logged on mount continues to be active when the component is unmounted.

## Solution

The solution includes a cleanup function within the returned value of the `useEffect` hook, ensuring that any side effects are cleaned up when the component unmounts.