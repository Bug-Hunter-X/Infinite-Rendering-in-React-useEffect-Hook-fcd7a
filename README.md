# Infinite Rendering Bug in React useEffect Hook

This repository demonstrates a common React bug: infinite rendering caused by a missing dependency array in the `useEffect` hook.

## Description
The `MyComponent` renders infinitely because the `useEffect` hook lacks a dependency array.  This causes the effect to run after every render, triggering a new render, leading to an infinite loop. The console shows that the component renders continuously without pausing. 

## Solution
Adding the `count` variable to the dependency array fixes the issue. Now the effect only runs when the value of `count` changes.