### ms.js
---
https://github.com/zeit/ms

```js
ms('2 days')
ms('1d')
ms('10h')
ms('2.5 hrs')
ms('2h')

ms(60000)
ms(2 * 60000)
ms(-3 * 60000)
ms(ms('10 hours'))

ms(60000, { long: true })
ms(2 * 60000, { long: true })
ms(-3 * 60000, { long: true })
ms(ms('10 hours'), { long: true })
```

```index.js
```

```tests.js
describe('ms(invalid inputs)', function() {
  it('should throw an error, when ms("")', function() {
    expect(function() {
      ms('');
    }).to.throwError();
  });
  
  it('should throw an error, when ms(undefined)', function() {
    expect(function() {
      ms(undefined);
    }).to.throwError();
  });
  
  it('should throw an error, when ms(null)', function() {
    expect(function() {
      ms([]);
    }).to.throwError();
  });
  
  it('should throw an error, when ms({})', function() {
    expect(function() {
      ms({});
    }).to.throwError();
  });
  
  it('should throw an error, when ms(NaN)', function() {
    expect(function() {
      ms(NaN);
    }).to.throwError();
  });
  
  it('should throw an error, when ms(Infinity)', function() {
    expect(function() {
      ms(Infinity);
    }).to.throwError();
  });
  
  it('should throw an error, when ms(-Indfinity)', function() {
    expect(function() {
      ms(-Infinity);
    }).to.throwError();
  });
});
```

