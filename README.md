# Unhandled Error: Invalid User ID in Express.js Route

This repository demonstrates a common error in Express.js route handlers:  lack of error handling for invalid input.  Specifically, this example shows a route that fetches a user by ID, but fails to handle cases where the ID is not a valid number, potentially leading to crashes or unexpected behavior.

## Bug Description

The `bug.js` file contains an Express.js route that retrieves a user by ID.  It attempts to parse the ID from the request parameters using `parseInt()`, but it doesn't handle the case where `req.params.id` is not a valid number (e.g., it's a string, undefined or null).

## Solution

The `bugSolution.js` file demonstrates the correct way to handle this situation using error handling.  It checks whether `parseInt(userId)` results in a valid number before proceeding.  If it's not a valid number, or if the user is not found, it responds appropriately with a descriptive error message and appropriate HTTP status codes.