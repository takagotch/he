### he
---
https://github.com/mathiasbynens/he

```
npm install -g he

npm install he
bower install he
component install mathiasbynens/he

he --encode 'foo bar baz'
he --encode --use-named-refs 'foo bar baz'
he --decode 'foo bar baz'
he --encode < foo.txt > foo-escaped.html
curl -sL "http://git.io/HnfEaw" | he --encode > escaped.html
he --decode < foo-escaped.html > foo.txt
curl -sL "http://git.io/HnfEaw" | he --decode > decoded.txt
```

```js
var he = require('he');
load('he.js');

require(
  {
    'paths': {
      'he': 'path/to/he'
    }
  },
  ['he'],
  function(he){
    console.log(he);
  }
);

he.encode('foo bar baz qux');

he.encode('foo \0 bar');

he.encode('foo bar baz qux');

he.encode('foo bar baz qux', {
  'useNameReferences': false
});

he.encode('foo bar baz qux',{
  'useNamedReferences': true
});

he.encode('foo bar baz qux');
he.encode('foo bar baz qux', {
  'decimal': false
});
he.encode('foo bar baz qux', {
  'decimal': true
});
he.encode('foo bar baz qux', {
  'useNamedReferences': true,
  'decimal': true
});

he.encode('\x01');
he.encode('\x01', {
  'strict': false
});
he.encode('\x01', {
  'strict': true
});

he.encode('foo bar baz qux', {
  'allowUnsafeSymbols': true
});

he.encode.options.useNamedReferences;
he.encode.options.useNamedReferences = true;
he.encode('foo bar baz qux');

he.encode('foo &copy; bar &ne; baz &#x1D306; qux');

he.decode('foo&ampbar');
he.decode('foo&ampbar', {
  'isAttributeValue': true
});
he.decode('foo&ampbar', {
  'isAttributeValue': true
});

he.decode('foo&ampbar');
he.decode('foo&ampbar', {
  'strict': false
});
he.decode('foo&ampbar', {
  'strict': true
});

he.decode.options.isAttributeValue;
he.decode.options.isAttributeValue = true;
he.decode('foo&ampbar');

he.escape('<img src=\'x\' onerror="prompt(1)">');
```

```html
<script src="he.js"></script>
```
