# React: Memory Leak with setInterval in useEffect

This repository demonstrates a common mistake in React: using `setInterval` within the `useEffect` hook without proper cleanup. This leads to memory leaks as the interval continues to run even after the component unmounts.

The `bug.js` file contains the buggy code. The `bugSolution.js` file demonstrates the correct way to use `setInterval` with `useEffect`, preventing memory leaks. 

## How to reproduce the bug

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the count increase every second.
5. Unmount the component (e.g., by navigating away or closing the browser tab).
6. The `setInterval` callback continues to run, leading to a memory leak.

## Solution

The `bugSolution.js` file provides the solution.  It demonstrates using `setInterval` with cleanup in useEffect.