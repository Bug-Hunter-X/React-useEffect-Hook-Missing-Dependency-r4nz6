# React useEffect Hook Missing Dependency

This repository demonstrates a common error in React applications involving the `useEffect` hook. The example showcases an incorrect dependency array in `useEffect`, leading to unexpected behavior and potential performance issues. The solution demonstrates how to correct the issue by including the necessary dependencies in the dependency array.

## Bug

The component uses the `useEffect` hook to log a message whenever the component renders. However, the dependency array is empty (`[]`), causing the effect to run only once on mount and not after state changes. Because `count` changes, the console.log should also run again, but it does not because of the missing dependency in the `useEffect`'s dependency array. This can lead to unexpected behavior when attempting to perform side effects based on state changes. 

## Solution

The solution correctly includes `count` in the dependency array. Now, the effect runs whenever `count` changes, reflecting the correct behavior of `useEffect`. By using a correct dependency array, you ensure that your side effect runs only when the specified values change.