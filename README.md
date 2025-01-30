# React useEffect Dependency Array Issue

This repository demonstrates a common error in React's `useEffect` hook: improperly specifying the dependency array.  The example showcases an infinite loop caused by an incomplete dependency array.

## Bug

The `bug.js` file contains a `useEffect` hook that attempts to increment a counter every second. However, the dependency array is empty (`[]`), meaning the effect runs only once after the component mounts.  This results in the counter being updated with the initial value of `count`, but never changing from that initial value.  This causes unexpected behavior.

## Solution

The `bugSolution.js` file corrects the issue by including `count` in the dependency array.  This ensures the effect runs whenever the `count` value changes, resulting in the correct counter behavior.

## How to reproduce the bug:

1. Clone the repository.
2. Navigate to the `bug` directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Observe the incorrect counter behavior.
6. Repeat steps 2-5, this time using `bugSolution.js` to observe the corrected behavior.
