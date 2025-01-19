# React useEffect Hook Bug

This repository demonstrates a common bug in React's `useEffect` hook where the dependency array is incorrectly specified, leading to the effect only running once during mounting.  The solution shows how to correctly use the dependency array to ensure the effect runs whenever a dependent state variable changes.

## Bug

The original `MyComponent` has a `useEffect` hook that aims to log a message whenever the `count` state variable is greater than 0. However, due to an incorrect dependency array, the `useEffect` hook only runs once during the initial render. The effect will not run again after incrementing the count because the if condition `count > 0` is evaluated only once, which only happens after the initial mount and not on every state change.

## Solution

The solution shows how to correctly specify the dependency array to ensure that the `useEffect` hook runs whenever the `count` state variable changes. By including `count` in the dependency array, the effect is triggered on every state update.  Additionally, the conditional logging is removed to showcase continuous monitoring of state changes.