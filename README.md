# Node.js Server Unresponsiveness
This repository demonstrates a common issue in Node.js applications: blocking the event loop with a long-running synchronous operation.  The server becomes unresponsive during the 5-second delay, unable to handle other requests.

## Bug Description
The provided `server.js` file contains a Node.js HTTP server that simulates a long-running task within the request handler. This task uses a `while` loop to block the event loop for 5 seconds, preventing the server from handling new requests during this time.

## Solution
The `serverSolution.js` file demonstrates how to fix this by using asynchronous operations.  Asynchronous programming prevents the event loop from being blocked, allowing the server to remain responsive even during long-running tasks.