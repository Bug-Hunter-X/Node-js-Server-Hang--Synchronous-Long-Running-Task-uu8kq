# Node.js Server Hang: Synchronous Long-Running Task

This repository demonstrates a common Node.js issue: a server hang caused by a long-running synchronous operation within the request handler.  The `server.js` file contains the buggy code, while `serverSolution.js` provides the solution.

**Problem:** The server's request handler performs a 5-second busy-wait, completely blocking the event loop.  During this time, the server is unresponsive to new requests.

**Solution:**  The solution involves refactoring the long-running task to be asynchronous using techniques like `setTimeout`, `setInterval`, or promises and async/await.