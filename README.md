# Inconsistent Browser Behavior with calc() in Media Queries

This repository demonstrates an uncommon issue related to the use of the CSS `calc()` function within media queries.  Specifically, it highlights inconsistent browser behavior when subtracting pixels from percentages inside a `calc()` expression used in a media query's conditional statement.

The problem often manifests when trying to set a breakpoint that dynamically adjusts based on the viewport width, but with a fixed pixel offset. For instance: `@media (max-width: calc(100vw - 100px))`

While the intention is clear, different browsers may interpret and handle this calculation differently, leading to unpredictable styling across various devices.

The `bug.css` file showcases the problematic code, while `bugSolution.css` offers an alternative approach to achieve a more consistent result across browsers.