# React useEffect Cleanup Function Error

This repository demonstrates a common error in React's `useEffect` hook, specifically related to the cleanup function and its dependency array.

## The Problem

The `bug.js` file contains a component that uses `useEffect` to update a counter every second. However, the dependency array is empty (`[]`), meaning the effect runs only once after the initial render and never cleans up. This causes the interval to persist even after the component unmounts, leading to a memory leak.

## The Solution

The `bugSolution.js` file corrects the issue by adding `count` to the dependency array. Now, the effect will run whenever `count` changes, and the cleanup function will be called when the component unmounts, clearing the interval properly.

## How to Reproduce

1. Clone the repository.
2. Navigate to the directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.

Observe the behavior in both `bug.js` and `bugSolution.js` to see the difference.
