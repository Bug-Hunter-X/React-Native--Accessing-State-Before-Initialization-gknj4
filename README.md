# React Native: Accessing State Before Initialization

This repository demonstrates a common error in React Native: accessing a component's state before it has been initialized. The `Bug.js` file showcases the problematic code, while `BugSolution.js` provides the corrected implementation.  The issue arises from attempting to use the state before the component mounts, resulting in `undefined` values and potential crashes.

## How to reproduce

1. Clone this repository.
2. Navigate to the directory in your terminal.
3. Run `npm install` to install dependencies.
4. Run the app (using expo or react-native run-android/ios).
5. Observe the error.  In the Bug.js version you should see an error relating to accessing 'count' before its defined.  The BugSolution.js version shows how to correct this.

## Solutions

The solution involves ensuring that state is accessed only after the component has mounted and the state has been properly initialized. This is typically done within the `useEffect` hook (for functional components) or after the `componentDidMount` lifecycle method (for class components).