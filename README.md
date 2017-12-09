# FileSystem Object Notation (FSON) RFC

### What is FSON?

FileSystem Object Notation or **FSON** is an open-standard format to describe JSON objects in a folder and file structure.

### Why?

 * So that real-time applications can edit each element individually without raising conflicts.
 * So that, in a UNIX system, only certain users/groups can read/write specific keys/values.
 * So that a GIT versioned FSON shows the evolution of each key/value as a single item.

### Rules

 * "X" becomes "_x"
 * "_" becomes "__"
 * " " becomes "-"

### Example

```javascript
{
	'name': 'John Doe',
	'age': 20,
	'colors': ['red', 'green', 'blue']
}
```

Is equivalent to:

* data/
  * age _(file contents: 20)_
  * name _(file contents: "John Doe")_
  * colors/
    * 0 _(file contents: "red")_
    * 1 _(file contents: "green")_
    * 2 _(file contents: "blue")_

