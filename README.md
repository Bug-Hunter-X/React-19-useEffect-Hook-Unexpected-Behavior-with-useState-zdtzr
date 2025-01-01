# React 19 useEffect Hook Unexpected Behavior with useState

This repository demonstrates a subtle bug encountered in React 19 concerning the interaction between the `useEffect` hook and `useState`.  The `useEffect` hook doesn't always update as expected when the state variable changes.

## Bug Description
The provided code snippet shows a simple counter component.  The `useEffect` hook is intended to log the updated count to the console whenever the `count` state variable changes.  However, in certain scenarios, particularly when updates happen rapidly or with complex state logic, the console logs may be inconsistent or incomplete.

## Solution
The solution involves ensuring the `useEffect` hook's dependency array includes all values that trigger changes in the component's behavior. In this example, adding the `count` variable to the dependency array ensures consistent behavior.