# Express.js JSON Body Parsing Error
This repository demonstrates a common issue in Express.js applications where parsing the JSON request body fails when the body is empty or contains invalid JSON data.  The server may log an empty object or throw an error, leading to a 500 Internal Server Error response to the client.

## Bug Description
The bug arises from not handling cases where the request body is malformed or missing. The `express.json()` middleware expects valid JSON; otherwise, it can't parse it correctly.

## Solution
The solution involves adding error handling to gracefully handle invalid JSON requests.  This ensures a more robust and user-friendly application.