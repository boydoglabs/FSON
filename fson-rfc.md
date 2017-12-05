# FSON RFC

### What is FSON?

FileSystem Object Notation or **FSON** is an open-standard format to describe JSON objects in a folder and file structure.

For example, the object:

```javascript
{
	'name': 'John Doe',
	'age': 20,
	'colors': ['red', 'green', 'blue']
}
```

Is equivalent in FSON to:

* data/
  * age _(file contents: 20)_
  * name _(file contents: "John Doe")_
  * colors/
    * 0 _(file contents: "red")_
    * 1 _(file contents: "green")_
    * 2 _(file contents: "blue")_
