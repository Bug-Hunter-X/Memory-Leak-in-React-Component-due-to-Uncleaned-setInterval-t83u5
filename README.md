# React setInterval Cleanup

This repository demonstrates a common React bug involving memory leaks caused by the improper use of `setInterval` within a component's `useEffect` hook. The `bug.js` file showcases the problematic code, while `bugSolution.js` provides a corrected version that prevents memory leaks.

## Problem
The original code uses `setInterval` to update a counter every second. However, it fails to properly clean up the interval when the component unmounts. This leads to the interval continuing to run indefinitely, even after the component is no longer displayed, resulting in a memory leak. 

## Solution
The corrected version includes a cleanup function within `useEffect`. This cleanup function clears the interval using `clearInterval` when the component is unmounted, preventing memory leaks.  This ensures that the interval is properly stopped when it's no longer needed.