# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook. The component renders repeatedly due to an improperly used `useEffect` hook, leading to an infinite loop and excessive console logging.

## Bug Description
The `useEffect` hook, without a dependency array, runs after every render. This creates a loop where the component re-renders, triggering the effect again, which causes another render, and so on. This results in an infinite render cycle.

## Solution
The solution is to provide a dependency array to the `useEffect` hook.  The dependency array specifies which values the effect should depend on.  The effect will only re-run when one of these values changes.

## How to reproduce the bug
1. Clone this repo
2. Run `npm install`
3. Run `npm start`
4. Observe the console spam and potentially a browser freeze.

## How to fix the bug
1. Examine the provided `bugSolution.js` file for the correct implementation of useEffect with a dependency array.