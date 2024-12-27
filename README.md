# Silent Crash on API Fetch in useEffect Hook

This repository demonstrates a common issue in React Native apps where an unhandled promise rejection within a `useEffect` hook can lead to a silent crash without any visible error message.  The problem occurs when fetching data from an external API, and an error occurs during the fetch process.

## Problem

The provided `App.js` attempts to fetch data from a JSONPlaceholder API.  If there's a network issue or the API is unavailable, the `fetch` promise rejects, but the `catch` block doesn't seem to handle the error properly, resulting in a silent crash on iOS.  There's no visible error message in the Expo Go app or the console. 

## Solution

The solution involves proper error handling within the `catch` block.  Instead of just logging the error to the console, the solution includes a more robust error handling mechanism. It displays an error message to the user, providing valuable feedback and improving the user experience.