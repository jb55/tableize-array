
# tableize-array

  Generate a table-friendly object by flattening the keys.

  Same as [tableize](https://github.com/segmentio/tableize) but with support
  for arrays

## Installation

```
$ npm install tableize-array
```

## Example

```js
var tableize = require('tableize-array');

var obj = tableize({
  user: {
    id: 123242123,

    name: {
      first: 'tobi',
      last: 'loki'
    },

    properties: {
      category: 'Buttons',
      label: 'Login'
    },

    context: {
      userAgent: 'Mozilla whatever'
    }
  }
});

console.log(obj);
```

yields:

```js
{ 'user.id': 123242123,
  'name.first': 'tobi',
  'name.last': 'loki',
  'properties.category': 'Buttons',
  'properties.label': 'Login',
  'context.userAgent': 'Mozilla whatever' }
```

# License

  MIT
