# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of error handling for invalid input.  The `bug.js` file contains code that attempts to fetch a user based on their ID, but it fails to handle cases where the ID is not a valid integer. This can lead to unexpected behavior or crashes in the application.

The `bugSolution.js` file shows how to fix this issue by adding proper error handling to gracefully manage invalid input and return appropriate error responses.

## How to reproduce the bug

1. Clone this repository.
2. Navigate to the `bug` directory.
3. Run `node bug.js`.
4. Send a request to `/users/abc` or `/users/123.45`. You will either get a server error or unpredictable behaviour.

## How to fix the bug

Refer to the `bugSolution.js` for the solution.  The solution implements error handling to check the validity of the user ID before attempting to use it, returning a meaningful error response if the ID is invalid.  The solution demonstrates that using `isNaN()` can be a useful tool for validating integer types.