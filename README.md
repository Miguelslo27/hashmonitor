# Hash Monitor

Hash Monitor is a powerfull tool to track hash changes, know if user go back or forwared and use methods like goTo, next or prev to navigate in hash history. Also contains an Event handler to handle onHashChange.

## How to install

```
$ npm install --save hashmonitor
```

## How to use

- Once you install the package you just have to incluide it

  ```
  const hm = require('hashmonitor');
  ```

  or

  ```
  import hm from 'hashmonitor';
  ```

- Then you have access to all the powerfull of hashmonitor in hm

  ```
  hm.onHashChange(callback);

  function callback(ev) {
    console.log(ev.hashmonitor);
    console.log(ev.hashmonitor.history); // Array of hashs history
    console.log(ev.hashmonitor.isBack);  // Boolean, if user went back (prev hash) it will be true, otherwise false
    console.log(ev.hashmonitor.oldHash); // support for IE allowed
    console.log(ev.hashmonitor.newHash); // support for IE allowed
  }

  // Methods (not implemented until next versions)
  // from v1.1.0
  hm.next() // Go to the next hash history point
  // from v1.1.0
  hm.prev() // Go to the prev hash history point
  // from v1.2.0
  hm.goTo([hash]) // Go to the given hash history point or create a new entry if not exists
  ```

## Créditos

- Miguel Sosa <miguel.sosa@appsxxi.com>

## Licencia

[MIT](https://opensource.org/licenses/MIT)