# React Router Dom Route Issue

This repository demonstrates a common issue encountered when using React Router Dom's `Routes` and `Route` components.  The problem arises from the order of routes defined and how the catch-all route (`*`) behaves.  This example showcases the incorrect implementation and its solution.

## Problem

The primary problem is that the catch-all route (`path="*"`) is placed before more specific routes. This causes the catch-all route to match every URL before any other routes have a chance to match, leading to the unexpected rendering of the 404 page even when navigating to a valid route. 

## Solution

The solution involves carefully ordering the routes.  The catch-all route should always be placed last in the `Routes` component. This ensures that it only matches when no other routes match, resulting in the correct behavior. 