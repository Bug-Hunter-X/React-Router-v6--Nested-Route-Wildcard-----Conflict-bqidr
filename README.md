# React Router v6 Nested Route Conflict

This repository demonstrates a common issue in React Router v6 involving nested routes and wildcard path parameters.  Specifically, a wildcard route (*) nested within a parent route can lead to unexpected behavior and errors if it overlaps with the parent route's path. The issue arises because the wildcard route will match all paths, preventing the parent route from ever being matched.

## Problem

The provided `bug.js` file contains an example where a nested wildcard route (`/about/*`) conflicts with a parent route (`/about`).  This setup results in the `/about` route being shadowed by the wildcard and causes issues when navigating to `/about`.

## Solution

The solution, in `bugSolution.js`, addresses this problem by carefully structuring the routes to avoid such conflicts. This often involves re-evaluating the routing structure or altering the wildcard usage to avoid route overlapping.