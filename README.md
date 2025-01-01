# React Native useEffect Hook with Empty Dependency Array Leads to Stale Data

This repository demonstrates a common issue in React Native development related to the use of the `useEffect` hook with an empty dependency array.  When using asynchronous operations or when external state changes, an empty dependency array can lead to stale data and incorrect UI updates. This example shows how this happens and provides a solution.

## Bug

The `bug.js` file contains the problematic code that utilizes `useEffect` with an empty dependency array.  This results in an API call happening only once on mount, and the component doesn't update even when the data from the API changes.  This leads to stale data being displayed.

## Solution

The `bugSolution.js` file shows the correct way to handle this. By adding the necessary state variable to the dependency array, the `useEffect` hook reruns whenever the state changes, ensuring the UI reflects the most up-to-date data. 

## Setup

1. Clone the repository
2. `npm install`
3. `expo start`