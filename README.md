# Uncommon HTML Bug: innerHTML Overwriting

This repository demonstrates an uncommon bug related to the incorrect usage of `innerHTML` in HTML to append content to an existing element.  The bug arises from misunderstanding how `innerHTML` replaces the entire content of an element instead of appending to it, if used incorrectly.

## Bug Description
The `innerHTML` property, when used to set content, overwrites all existing content. Attempting to append by using += may lead to unexpected behavior due to this replacement.  This example shows how using `innerHTML +=` repeatedly results in only the last addition being visible.  This behaviour is not intuitive, hence the uncommon nature of the bug.

## How to Reproduce
1. Open `bug.html` in a web browser.
2. Observe that only the last paragraph added using `innerHTML +=` is displayed, while the previous addition is replaced.

## Solution
The solution involves using `insertAdjacentHTML` which provides more granular control over adding content to an element.  Or, appendChild with created elements.

## License
MIT