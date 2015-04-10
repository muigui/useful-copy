# useful-copy

  useful deep/shallow copy/update

## Installation

```shell

    >$ npm install useful-copy

```

## Test

```shell

    useful-copy>$ npm test

```

## Build

if you want to convert useful-copy into es5, you can simply run:

```shell

    useful-copy>$ npm run build

```

## API

### copy( target:Object, source:Object[, no_overwrite:Boolean] ):Object
Copies the properties – accessible via `Object.keys` – from the `source` Object to the `target` Object and returns the `target` Object.

#### Example:

```javascript

	var copy = require( 'useful-copy' );

    var foo = { one : 1, two : 2, three : 3 },
        bar = copy( {}, foo );

    bar          // returns => { "one" : 1, "two" : 2, "three" : 3 }

    foo === bar  // returns => false

    copy( foo, { three : 3.3, four : 4 }, true ); // returns => { "one" : 1, "two" : 2, "three" : 3, "four" : 4 }

```

### copy.merge( target:Array|Object, source:Array|Object ):Boolean
Performs a "deep copy" of all the properties in `source` to `target`, so that `target` does not reference any child Arrays and/ or Objects that belong to `source`.

### copy.update( target:Array|Object, source:Array|Object ):Boolean
Performs a "deep copy" of all the properties in `source` **that are not already contained in** `target`, so that `target` does not reference any child Arrays and/ or Objects that belong to `source`.

This works similarly to `copy.merge` except that existing properties are not overwritten.

## License

(The MIT License)

Copyright (c) 2011 christos "constantology" constandinou http://muigui.com

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the 'Software'), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

![Analytics](https://ga-beacon.appspot.com/UA-15072756-2/muigui/useful-copy/readme)
