# React Router v6 Catch-all Route Issue

This repository demonstrates a common issue encountered when using catch-all routes ("/*") in React Router v6.  The catch-all route unexpectedly intercepts all paths, even when more specific routes should be matched first. This leads to incorrect routing and unexpected behavior.

## Problem

In the provided example, the catch-all route (`/*`) intended to handle 404 errors, prevents other routes from being matched, even when a path matches a more specific route.  This is a departure from previous versions of React Router.

## Solution

The solution involves re-ordering the routes.  Placing the catch-all route at the very end of the `<Routes>` component ensures that it only matches when no other routes are applicable.