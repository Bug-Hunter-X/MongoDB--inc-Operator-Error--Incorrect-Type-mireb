# MongoDB $inc Operator Error: Incorrect Type

This example demonstrates an incorrect use of the `$inc` operator in a MongoDB update operation. The `$inc` operator is used to increment a numerical field by a specified value. However, providing a string value will cause an error.

## Bug Description

The bug involves using a string value ("1") instead of a numerical value (1) with the `$inc` operator. This results in an error because the `$inc` operator expects a number.

## Solution

The solution is to use a numerical value (1) instead of a string value ("1") when using the `$inc` operator:
```javascript
db.collection.updateOne({"_id": ObjectId("651234567890")}, {"$inc": {"count": 1}});
```