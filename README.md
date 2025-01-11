# Node.js Server Port Already in Use

This repository demonstrates a common error in Node.js: attempting to start a server on a port that's already in use.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides a robust solution.

## Problem

When you run `bug.js`, if port 8080 is occupied by another process, the server will fail to start and throw an error. This can be frustrating, especially in production environments.

## Solution

The `bugSolution.js` file demonstrates a more resilient approach. It uses a `try...catch` block to handle the `EADDRINUSE` error gracefully. Additionally, it includes a small delay to allow the system to release the port before attempting to start the server again.