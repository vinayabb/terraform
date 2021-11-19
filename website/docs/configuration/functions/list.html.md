---
layout: "language"
page_title: "list - Functions - Configuration Language"
sidebar_current: "docs-funcs-collection-list"
description: |-
  The list function constructs a list from some given elements.
---

# `list` Function

-> **Note:** This page is about Terraform 0.12 and later. For Terraform 0.11 and
earlier, see
[0.11 Configuration Language: Interpolation Syntax](../../configuration-0-11/interpolation.html).

The `list` function is no longer available. Prior to Terraform v0.12 it was
the only available syntax for writing a literal list inside an expression,
but Terraform v0.12 introduced a new first-class syntax.

To update an expression like `list(a, b, c)`, write the following instead:

```
tolist([a, b, c])
```

The `[ ... ]` brackets construct a tuple value, and then the `tolist` function
then converts it to a list. For more information on the value types in the
Terraform language, see [Type Constraints](../types.html).

## Related Functions

* [`concat`](./concat.html) produces a new list by concatenating together the
  elements from other lists.
* [`tolist`](./tolist.html) converts a set or tuple value to a list.