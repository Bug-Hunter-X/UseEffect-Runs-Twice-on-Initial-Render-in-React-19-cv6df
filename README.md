# React 19 useEffect Bug

This repository demonstrates a subtle bug encountered in React 19 where the `useEffect` hook runs twice during the initial render.  This can lead to unexpected side effects and debugging challenges.

## Bug Description
The `useEffect` hook, even with an empty dependency array, is unexpectedly called twice upon the initial mount of the component. This is not standard React behavior and can cause issues when performing side effects such as API calls or DOM manipulations.

## Bug Reproduction
1. Clone this repository.
2. Run `npm install` to install the dependencies.
3. Run `npm start` to start the development server.
4. Observe the console; you'll see 'Effect ran!' logged twice.

## Solution
The solution involves carefully examining the component's rendering logic and identifying any potential sources of re-renders during mount. In this case, it is a simple typo that causes this issue, resulting in an extra render before settling to the correct state. The solution is provided in `bugSolution.js`.