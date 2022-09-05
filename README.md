# The Node.js & Javascript Course



# Table of Contents



- Testing
  - Mocha
    - Assertions
    - Async Await
    - Hooks
  - Chai
  - Chai HTTP



----





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



---



### Assertions

For assertions we will using chai.js



---



### Async Await

Here is an example using Async Await :

```javascript
beforeEach(async function () {
  await db.clear();
  await db.save([tobi, loki, jane]);
});

describe('#find()', function () {
  it('responds with matching records', async function () {
    const users = await db.find({type: 'User'});
    users.should.have.length(3);
  });
});
```



---



### Hooks

For helping the development mocha provide hooks :

```javascript
describe('hooks', function () {
  before(function () {
    // runs once before the first test in this block
  });

  after(function () {
    // runs once after the last test in this block
  });

  beforeEach(function () {
    // runs before each test in this block
  });

  afterEach(function () {
    // runs after each test in this block
  });

  // test cases
});
```

