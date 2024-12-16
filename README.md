# React useState Double Update Bug

This repository demonstrates a subtle bug related to the React `useState` hook. When `setCount` is called twice in rapid succession within a single event handler, the second update might overwrite the first, leading to unexpected results.

## Bug Description

The bug lies in how React batches state updates.  If you call `setCount` multiple times in a single event, React might not apply all the updates correctly. This typically leads to a value that is unexpectedly lower than expected. 

## Solution

The solution is to use functional updates with `setCount`. This approach ensures that `setCount` is always based on the latest state value.