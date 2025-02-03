# React useEffect setInterval Memory Leak
This example demonstrates a common mistake in React components when using the `useEffect` hook with `setInterval`.  Forgetting to clear the interval before the component unmounts leads to a memory leak. The solution showcases the correct way to use `setInterval` within `useEffect` to avoid this issue.

## Bug
The `bug.js` file contains a React component that uses `setInterval` to update a count every second. However, it fails to clear the interval when the component unmounts, causing a memory leak.

## Solution
The `bugSolution.js` file provides the corrected component. It uses the return value of `useEffect` to clear the interval before the component unmounts, preventing the memory leak.