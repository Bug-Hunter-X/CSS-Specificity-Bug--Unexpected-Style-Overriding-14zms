# CSS Specificity Bug: Unexpected Style Overriding

This repository demonstrates a common issue in CSS related to selector specificity. The goal is to style two '.box' elements differently based on their position in the HTML, but due to how CSS specificity works, only the second '.box' is correctly styled, overriding the style of the first one.

## Bug Description
The bug lies in the specificity of the CSS selectors. The selector `#container .box` is less specific than `#container2 .box`.  Because of this, the styles defined for `#container2 .box` will override the styles for `#container .box`.

## How to Reproduce
1. Clone this repository.
2. Open `index.html` in your web browser.
3. Observe that only the second `.box` element is styled as intended; the first `.box` inherits styles from the second one because of the specificity issue.

## Solution
The provided `bugSolution.css` file demonstrates how to resolve the specificity problem by applying a more specific selector to the first `.box` element.
