# Node.js Unhandled Exception Example
This repository demonstrates a common error in Node.js applications: unhandled exceptions causing server crashes.  The `bug.js` file shows a server vulnerable to this, while `bugSolution.js` presents a more robust solution.

## Bug
The original server lacks error handling. Any unexpected exception (e.g., accessing a non-existent file) will terminate the server abruptly.

## Solution
The improved server uses `try...catch` blocks and event listeners (`'uncaughtException'`, `'unhandledRejection'`) to gracefully handle unexpected errors, logging details and preventing the server from crashing.