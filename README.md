# React setInterval Memory Leak
This repository demonstrates a common React bug involving memory leaks when using `setInterval` within the `useEffect` hook without proper cleanup.

The `bug.js` file showcases the flawed implementation.  The `setInterval` is started, but there's no mechanism to stop it when the component unmounts. This results in the interval continuing to run indefinitely, leading to memory leaks.

The `bugSolution.js` file provides the corrected version, demonstrating how to use the return value of `useEffect` to add a cleanup function that clears the interval.

## How to Reproduce
1. Clone this repository
2. Navigate to the directory in your terminal
3. Run `npm install`
4. Run `npm start`
5. Observe the memory usage in your browser's developer tools. The unfixed version will show a continuous increase in memory usage, highlighting the memory leak.