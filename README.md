# Unhandled Promise Rejection in Express.js Async Route Handler

This repository demonstrates a common error in Express.js applications where unhandled promise rejections in asynchronous route handlers can lead to server crashes.  The provided `bug.js` file showcases the issue, while `bugSolution.js` offers a corrected implementation.

## Problem

The problem lies in how errors are handled within asynchronous operations within Express.js route handlers.  If an error occurs within a `then()` block of a promise, the error is not properly caught and handled, leading to an unhandled promise rejection that can crash the Node.js process.

## Solution

The solution involves using appropriate error handling mechanisms to catch and handle errors within asynchronous route handlers. This includes utilizing `.catch()` to handle rejections, and more robust error management techniques to prevent server crashes.