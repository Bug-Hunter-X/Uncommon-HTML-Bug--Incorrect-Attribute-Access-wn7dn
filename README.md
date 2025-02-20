# Uncommon HTML Bug: Incorrect Attribute Access

This repository demonstrates an uncommon bug related to accessing HTML element attributes.  The bug arises from using `getAttributeNode().nodeValue` instead of the more robust `getAttribute()` method.  The `getAttributeNode()` method returns a Node object, which can be null if the attribute isn't found, causing an error when attempting to access `nodeValue`. The `getAttribute()` method is more forgiving, returning null if the attribute doesn't exist.

## Bug Description

The bug occurs when attempting to retrieve the value of an attribute using `getAttributeNode().nodeValue`. If the specified attribute does not exist on the element, this method will throw an error.  A more robust solution uses `getAttribute()`, which gracefully handles cases where the attribute is absent.

## Solution

The solution involves using the `getAttribute()` method to retrieve the attribute value. This method returns null if the attribute doesn't exist, preventing errors. The solution demonstrates how to gracefully handle the case where the attribute may be missing.