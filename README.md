# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications: an infinite loop caused by a missing dependency in the `useEffect` hook.

## Bug Description
The `useEffect` hook is used to perform side effects after a component renders. However, if the effect's dependencies array is missing or incorrect, the effect may run infinitely, leading to performance issues and unexpected behavior.

## Bug Reproduction
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the console log.  The message 'Component rendered with count:' will repeatedly print to the console as the component renders endlessly.

## Bug Solution
The solution is to include `count` in the dependencies array for the `useEffect` hook. This ensures that the effect only re-runs when `count` changes. See `bugSolution.js` for the corrected code.