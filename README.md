# Missing Cleanup Function in React's useEffect Hook

This repository demonstrates a common error in React's `useEffect` hook: forgetting to include a cleanup function.  The absence of a return statement within `useEffect` can lead to memory leaks and unexpected behavior if the component unmounts before cleanup actions are performed.  The `bug.js` file showcases the error; `bugSolution.js` provides the corrected version.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs and the component's behavior.

## Solution

The corrected code in `bugSolution.js` includes a return statement within `useEffect`.  This return statement provides a cleanup function that is automatically called when the component unmounts, ensuring proper resource cleanup and avoiding potential issues.