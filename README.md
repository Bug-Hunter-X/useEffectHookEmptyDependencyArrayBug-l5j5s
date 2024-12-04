# React useEffect Hook Bug

This repository demonstrates a common React bug related to the `useEffect` hook and its dependency array. The `useEffect` hook with an empty dependency array runs only once after the initial render.  This example shows how this can lead to unexpected behavior or infinite rendering loops if not properly handled.

## Bug Description

The provided `MyComponent` uses `useEffect` with an empty dependency array (`[]`).  This is incorrect if the intention is to run the effect on every state change.  The effect only runs once when the component mounts, even if the state (`count`) changes. This may lead to the effect not reflecting changes.

## Bug Solution

The solution is to include the `count` state variable in the dependency array.  This ensures the effect is triggered when the state changes.