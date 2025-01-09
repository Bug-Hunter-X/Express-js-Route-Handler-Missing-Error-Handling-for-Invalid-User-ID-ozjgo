# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the `/users/:id` route attempts to parse the `id` parameter as an integer without checking for potential errors (e.g., non-numeric input). This can lead to crashes or unexpected behavior.

## Bug

The `bug.js` file contains the erroneous code.  The route handler doesn't handle cases where `req.params.id` is not a valid integer, resulting in an error if a non-numeric ID is passed.

## Solution

The `bugSolution.js` file provides a corrected version of the code.  It adds input validation to ensure that `req.params.id` is a number before attempting to parse it.  This prevents errors and provides a more robust user experience.