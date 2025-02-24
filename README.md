# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js where a long-running operation in a request handler can block the event loop, causing the server to become unresponsive.  The example uses a synchronous `while` loop to simulate this behavior.

## Problem
The `bug.js` file contains a simple HTTP server with a request handler that performs a long-running operation. This operation blocks the event loop, preventing the server from handling subsequent requests.  This can lead to timeouts and a poor user experience.

## Solution
The `bugSolution.js` demonstrates the correct approach to handle long-running operations asynchronously using promises, async/await, or workers to avoid blocking the event loop.