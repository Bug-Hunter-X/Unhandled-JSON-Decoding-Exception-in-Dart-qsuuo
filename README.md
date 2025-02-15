# Unhandled JSON Decoding Exception in Dart

This repository demonstrates a common error in Dart applications involving asynchronous network requests and JSON parsing. The `bug.dart` file contains code that fetches data from a server, parses it as JSON, and handles potential HTTP errors. However, it neglects to handle the `FormatException` that can occur if the server returns invalid JSON.

The `bugSolution.dart` file provides a corrected version that robustly handles this exception, preventing app crashes and improving user experience.

## How to Reproduce the Bug

1. Run `bug.dart`.
2. If the API returns invalid JSON (e.g., due to a server-side error), the app will crash with a `FormatException`.

## Solution

The solution involves using a `try-catch` block to specifically handle `FormatException` during JSON decoding.