# muller

Simple demonastration of [Muller's Recurrence](http://latkin.org/blog/2014/11/22/mullers-recurrence-roundoff-gone-wrong/) problem which shows the floating point roundoff errors.

## Use

You can get this example via NPM
```sh
npm install muller
```

This example is implemented using in 3 ways:
* using native Number class
* using [bignumber.js](https://github.com/MikeMcl/bignumber.js/)
* using [decimal.js](https://github.com/MikeMcl/decimal.js/)

In order to run it this example use the following command

```sh
node index.js [library] [decimal_places]
```

library can be "dec" or "big" for decimal.js or bignumber.js respectively. If it isn't provided native Number is used.

decimal_places is used for bignumber.js and represents the maximum number of decimal places of the results of operations. (default values is 20)

## Benchmarks

The tests were done using Intel® Core™ i7-4702MQ @ 2.20 Ghz with default number of decimal places for bignumber.js

### native
```sh
real    0m0.299s
user    0m0.000s
sys     0m0.031s
```
### bignumber.js
```sh
real    0m28.282s
user    0m0.000s
sys     0m0.015s
```
### decimal.js
```sh
real    0m25.758s
user    0m0.015s
sys     0m0.015s
```
