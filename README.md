# React Native Dimensions API Async Issue

This repository demonstrates a common issue encountered when using the `Dimensions` API in React Native to obtain screen dimensions, particularly on Android devices. The problem arises from the asynchronous nature of the API, where accessing dimensions immediately after calling `Dimensions.get()` may result in incorrect or undefined values.

## Problem
The `Dimensions.get()` method is asynchronous; the values are not immediately available. Accessing the width and height properties before the values are populated will lead to incorrect calculations or crashes.

## Solution
The provided solution uses the `useEffect` hook to ensure the dimensions are fetched asynchronously, and the component re-renders with the correct values once they're available.