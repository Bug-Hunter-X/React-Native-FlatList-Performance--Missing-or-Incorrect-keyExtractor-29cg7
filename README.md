# React Native FlatList Performance Issue: Missing keyExtractor

This repository demonstrates a common performance problem in React Native's FlatList component and its solution.  The problem arises from the absence of a properly implemented `keyExtractor` function, leading to inefficient updates and potential performance bottlenecks when rendering large datasets.

## Problem

Without a unique key for each item in the FlatList's data, React Native struggles to identify which items have changed. This causes unnecessary re-renders of the entire list, significantly impacting performance, especially with many items.

## Solution

The solution involves providing a `keyExtractor` function to the FlatList.  This function takes an item from your data array and returns a unique identifier for that item.  This allows React Native to efficiently update only the necessary components, dramatically improving performance.

## How to Run

1. Clone the repository.
2. Navigate to the project directory in your terminal.
3. Run `npm install` to install the dependencies.
4. Run `npx react-native run-android` or `npx react-native run-ios` to start the app.