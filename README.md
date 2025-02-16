# Unnecessary Re-renders in React 19 useEffect Hook

This repository demonstrates a common React 19 issue where the `useEffect` hook causes unnecessary re-renders and console spam.  The example shows an effect that runs after every render, even when the count doesn't change. This is inefficient and can lead to performance problems.  The solution shows how to use the effect's dependency array to control when the effect runs.

## Bug
The `bug.js` file contains the buggy component. The `useEffect` hook runs after every render, logging to the console. This is inefficient and should be avoided for production environments.

## Solution
The `bugSolution.js` file contains the corrected component. The dependency array `[count]` is used to control when the effect runs, only executing when the `count` value changes.