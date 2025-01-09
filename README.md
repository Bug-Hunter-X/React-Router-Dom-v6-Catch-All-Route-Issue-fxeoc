# React Router Dom v6 Catch All Route Issue

This repository demonstrates a common issue encountered when using catch-all routes (`/*`) in React Router v6.  The issue is that the catch-all route might not work as expected, failing to match paths not covered by other routes.  The solution provided fixes this behaviour.

## Problem:

The `/*` route in the provided `App.js` example is intended to catch any unmatched routes and display a 404 page.  However, due to the order of routes, other routes may take precedence, rendering the catch-all ineffective.

## Solution:

The solution provided in `AppSolution.js` moves the catch-all route to the end of the route list.  By placing the catch-all route last, it ensures that it only matches paths not already matched by the other, more specific routes.