# Uncommon HTML Bug: Setting innerHTML to null

This repository demonstrates an uncommon bug in HTML related to setting the `innerHTML` property of an element to `null`.  While it might seem intuitive that this would remove the element, it only clears its content, leaving an empty element in the DOM.  This can lead to subtle and hard-to-debug issues.

The `bug.html` file shows the problematic code, and `bugSolution.html` provides the corrected version.

## Bug Description

Setting `innerHTML` to `null` on an element does *not* remove the element from the DOM. It simply removes the element's contents leaving behind an empty element. This behavior can be unexpected, leading to issues with element manipulation and DOM traversal.

## Solution

The correct way to remove an element's content (or the element entirely) is to use different methods: To clear the content, set `innerHTML` to an empty string (`""`). To remove the element, use the `removeChild` method of its parent node. 