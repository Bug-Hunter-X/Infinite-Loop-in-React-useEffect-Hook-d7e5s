# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug causes an infinite loop due to an incorrectly specified dependency array.

## Bug Description
The `useEffect` hook is used to perform side effects after a component renders.  If the dependency array is incorrect, it can lead to unintended re-renders and potentially an infinite loop.  In this example, the `useEffect` hook is unintentionally triggering a re-render after every state update.

## How to Reproduce
Clone this repository and run `npm install` to install dependencies. Then, run `npm start` to start the development server. You'll observe the browser console logging continuously, indicating the infinite loop.

## Solution
The solution involves correctly specifying the dependency array for the `useEffect` hook. By only including `count` in the array, the effect will only run when the `count` state variable changes, preventing the infinite loop.