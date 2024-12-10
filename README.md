# Unhandled Promise Rejection in useEffect Hook - React Native

This repository demonstrates a common issue in React Native applications where an unhandled promise rejection within a `useEffect` hook causes the app to crash on Android.  The problem is exacerbated by unclear error messages, making debugging challenging.

## Problem Description

A React Native component fetches data from an API using `fetch` within a `useEffect` hook.  If the API request fails, a promise rejection occurs.  On Android, this rejection is not handled gracefully and the app crashes.

## Solution

The solution involves properly handling potential errors within the `async/await` block and providing more robust error handling to prevent app crashes.  The `try...catch` block catches the error, providing a user-friendly error message instead of a crash.