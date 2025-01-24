# React useEffect Hook Bug

This repository demonstrates a common bug in React's `useEffect` hook: an infinite loop caused by a missing dependency in the dependency array. 

## Bug Description

The `useEffect` hook is used to perform side effects after every render.  When a state variable is used within the `useEffect` function and it is *not* included in the dependency array, the effect will run repeatedly, leading to an infinite render loop and potential crashes.  This example illustrates this problem with the `count` state variable.