# The Node.js & Javascript Course







# Testing



## Mocha

Execute this command to install mocha

```bash
$ npm install mocha
$ mkdir test
```

Create test.js inside test directory and write this code :

```js
var assert = require('assert');
describe('Array', function () {
  describe('#indexOf()', function () {
    it('should return -1 when the value is not present', function () {
      assert.equal([1, 2, 3].indexOf(4), -1);
    });
  });
});
```

Back in the terminal:

```bash
$ ./node_modules/mocha/bin/mocha

  Array
    #indexOf()
      ✓ should return -1 when the value is not present


  1 passing (9ms)
```

Set up a test script in package.json:

```json
"scripts": {
  "test": "mocha"
}
```

Then run tests with:

```bash
$ npm test
```