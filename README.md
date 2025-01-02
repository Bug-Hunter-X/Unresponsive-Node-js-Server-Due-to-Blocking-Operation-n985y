# Unresponsive Node.js Server Due to Blocking Operation

This repository demonstrates a common issue in Node.js where a long-running synchronous operation blocks the event loop, making the server unresponsive.

The `blockingServer.js` file shows the problematic code.  The `nonblockingServer.js` provides the solution.

## How to Reproduce

1. Clone this repository.
2. Run `node blockingServer.js`.
3. Try to access `http://localhost:3000/` in your browser. You'll notice that the server becomes unresponsive for approximately 5 seconds.
4. Run `node nonblockingServer.js`. The server will remain responsive even during the long running task.

## Solution

The solution involves using asynchronous operations to avoid blocking the event loop.  The `nonblockingServer.js` shows how to do this.