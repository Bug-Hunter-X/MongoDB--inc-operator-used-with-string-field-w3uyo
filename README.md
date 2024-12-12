# MongoDB $inc operator used with string field

This repository demonstrates a common error in MongoDB when using the `$inc` operator with a string field. The `$inc` operator is designed for numerical fields and will throw an error if used with a string field. 

The `bug.js` file contains the erroneous code, while `bugSolution.js` provides the corrected implementation.

## Bug
The bug is in the incorrect usage of `$inc` with string fields. Attempting to increment a string field using `$inc` results in an error.

## Solution
The solution involves ensuring that the field you are incrementing is of a numerical type (e.g., NumberInt, NumberLong, or a number). If the field is a string, it must be converted to a number before applying the `$inc` operator or use an alternative approach that handles strings appropriately.