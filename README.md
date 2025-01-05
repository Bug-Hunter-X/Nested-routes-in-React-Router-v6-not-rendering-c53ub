# React Router v6 Nested Routes Issue

This repository demonstrates a problem with nested routes in React Router v6.  Nested routes are defined, but they are not rendering correctly.  The parent route renders without issue.

## Problem Description

When navigating to nested routes, only the parent route's component is rendered. The nested components are not displayed, despite seemingly correct configuration.

## Solution

The issue was resolved by ensuring the `useLocation` hook was used correctly within nested components that needed access to URL parameters.   Additionally, the order of routes within the `Routes` component is significant and impacted whether or not the nested routes were matched.