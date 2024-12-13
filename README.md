# React Router v6 Catch-all Route Issue

This repository demonstrates a problem with the catch-all route (`/*`) in React Router v6.  Other routes seem to always take precedence, preventing the catch-all route from handling unmatched paths.

The issue is that even though the `/*` route should be the fallback, it's not triggered.  This can lead to unexpected behavior where 404 pages are not displayed for non-matching paths.

## Solution

The solution involves understanding the order of route matching in React Router v6 and ensuring that the catch-all route is truly the last resort.  This is achieved by placing the `/*` route as the last route defined in the `Routes` component.  While seemingly straightforward, this is often overlooked.