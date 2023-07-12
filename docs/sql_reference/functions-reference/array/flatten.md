---
layout: default
title: FLATTEN
description: Reference material for FLATTEN function
grand_parent: SQL functions
parent: Array functions
---

# FLATTEN

Converts an array of arrays into a flat array. This means for every element that is an array, this function extracts its elements into the new array. The resulting flattened array contains all the elements from all source arrays.

The function:

* Applies to any depth of nested arrays.
* Does not change arrays that are already flat.

## Syntax
{: .no_toc}

```sql
FLATTEN(<arr_of_arrs>)
```

| Parameter       | Description                          |
| :--------------- | :------------------------------------ |
| `<arr_of_arrs>` | The array of arrays to be flattened. |

## Return Types
The return type for this function is `ARRAY`.

## Example
{: .no_toc}
The following example flattens multiple arrays of video game levels: 

```sql
SELECT
	flatten([ [ [ 1, 2 ] ], [ [ 2, 3 ], [ 3, 4 ] ] ])
```

**Returns**: `[1, 2, 2, 3, 3, 4]`