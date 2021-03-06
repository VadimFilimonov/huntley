### Table of Contents

*   [add][1]
    *   [Parameters][2]
    *   [Examples][3]
*   [chunk][4]
    *   [Parameters][5]
    *   [Examples][6]
*   [constant][7]
    *   [Parameters][8]
    *   [Examples][9]
*   [defaultTo][10]
    *   [Parameters][11]
    *   [Examples][12]
*   [divide][13]
    *   [Parameters][14]
    *   [Examples][15]
*   [drop][16]
    *   [Parameters][17]
    *   [Examples][18]
*   [dropRight][19]
    *   [Parameters][20]
    *   [Examples][21]
*   [gt][22]
    *   [Parameters][23]
    *   [Examples][24]
*   [head][25]
    *   [Parameters][26]
    *   [Examples][27]
*   [identity][28]
    *   [Parameters][29]
    *   [Examples][30]
*   [initial][31]
    *   [Parameters][32]
    *   [Examples][33]
*   [isArray][34]
    *   [Parameters][35]
    *   [Examples][36]
*   [isMap][37]
    *   [Parameters][38]
    *   [Examples][39]
*   [isNil][40]
    *   [Parameters][41]
    *   [Examples][42]
*   [isNull][43]
    *   [Parameters][44]
    *   [Examples][45]
*   [isObjectLike][46]
    *   [Parameters][47]
    *   [Examples][48]
*   [isString][49]
    *   [Parameters][50]
    *   [Examples][51]
*   [isUndefined][52]
    *   [Parameters][53]
    *   [Examples][54]
*   [last][55]
    *   [Parameters][56]
    *   [Examples][57]
*   [lt][58]
    *   [Parameters][59]
    *   [Examples][60]
*   [max][61]
    *   [Parameters][62]
    *   [Examples][63]
*   [mean][64]
    *   [Parameters][65]
    *   [Examples][66]
*   [min][67]
    *   [Parameters][68]
    *   [Examples][69]
*   [multiply][70]
    *   [Parameters][71]
    *   [Examples][72]
*   [noop][73]
    *   [Examples][74]
*   [nth][75]
    *   [Parameters][76]
    *   [Examples][77]
*   [partition][78]
    *   [Parameters][79]
    *   [Examples][80]
*   [reverse][81]
    *   [Parameters][82]
    *   [Examples][83]
*   [size][84]
    *   [Parameters][85]
    *   [Examples][86]
*   [stubArray][87]
    *   [Examples][88]
*   [stubFalse][89]
    *   [Examples][90]
*   [stubObject][91]
    *   [Examples][92]
*   [stubString][93]
    *   [Examples][94]
*   [stubTrue][95]
    *   [Examples][96]
*   [subtract][97]
    *   [Parameters][98]
    *   [Examples][99]
*   [sum][100]
    *   [Parameters][101]
    *   [Examples][102]
*   [tail][103]
    *   [Parameters][104]
    *   [Examples][105]
*   [uniq][106]
    *   [Parameters][107]
    *   [Examples][108]
*   [upperFirst][109]
    *   [Parameters][110]
    *   [Examples][111]

## add

Adds two numbers.

### Parameters

*   `augend` **[number][112]** The first number in an addition.
*   `addend` **[number][112]** The second number in an addition.

### Examples

```javascript
add(6, 4);
// => 10
```

Returns **[number][112]** Returns the total.

## chunk

Creates an array of elements split into groups the length of `size`. If `array` can't be split evenly, the final chunk will be the remaining elements.

### Parameters

*   `array` **[Array][113]** The array to process.
*   `size` **[number][112]** The length of each chunk. (optional, default `1`)

### Examples

```javascript
chunk(['a', 'b', 'c', 'd'], 2);
// => [['a', 'b'], ['c', 'd']]

chunk(['a', 'b', 'c', 'd'], 3);
// => [['a', 'b', 'c'], ['d']]
```

Returns **[Array][113]** Returns the new array of chunks.

## constant

Creates a function that returns `value`.

### Parameters

*   `value` **any** The value to return from the new function.

### Examples

```javascript
const func = constant({ a: 1 });
func();
// => { a: 1 }
```

Returns **[Function][114]** Returns the new constant function.

## defaultTo

Checks `value` to determine whether a default value should be returned in its place.
The `defaultValue` is returned if `value` is `NaN`, `null`, or `undefined`.

### Parameters

*   `value` **any** 
*   `defaultValue` **any** 

### Examples

```javascript
defaultTo(1, 10);
// => 1

defaultTo(undefined, 10);
// => 10
```

Returns **[boolean][115]** 

## divide

Divide two numbers.

### Parameters

*   `dividend` **[number][112]** 
*   `divisor` **[number][112]** 

### Examples

```javascript
divide(6, 4);
// => 1.5
```

Returns **[number][112]** Returns the quotient

## drop

Creates a slice of `array` with `n` elements dropped from the beginning.

### Parameters

*   `array` **[Array][113]** The array to query.
*   `n` **[number][112]** The number of elements to drop. (optional, default `1`)

### Examples

```javascript
drop([1, 2, 3]);
// => [2, 3]

drop([1, 2, 3], 2);
// => [3]

drop([1, 2, 3], 5);
// => []

drop([1, 2, 3], 0);
// => [1, 2, 3]
```

Returns **[Array][113]** Returns the slice of `array`.

## dropRight

Creates a slice of `array` with `n` elements dropped from the end.

### Parameters

*   `array` **[Array][113]** The array to query.
*   `n` **[number][112]** The number of elements to drop. (optional, default `1`)

### Examples

```javascript
dropRight([1, 2, 3]);
// => [1, 2]

dropRight([1, 2, 3], 2);
// => [1]

dropRight([1, 2, 3], 5);
// => []

dropRight([1, 2, 3], 0);
// => [1, 2, 3]
```

Returns **[Array][113]** Returns the slice of `array`.

## gt

Checks if `value` is greater than `other`.

### Parameters

*   `value` **any** The value to compare.
*   `other` **any** The other value to compare.

### Examples

```javascript
gt(3, 1);
// => true

gt(3, 3);
// => false

gt(1, 3);
// => false
```

Returns **[boolean][115]** Returns true if value is greater than other, else false.

## head

Gets the first element of array.

### Parameters

*   `array` **[Array][113]** 

### Examples

```javascript
head([1, 2, 3]);
// => 1
```

Returns **any** 

## identity

This method returns the first argument it receives.

### Parameters

*   `value` **any** 

### Examples

```javascript
identity('Run');
// => 'Run'

identity((v) => v)('Run');
// => 'Run'

const object = { 'a': 1 };
identity(object) === object;
// => true
```

Returns **any** 

## initial

Gets all but the last element of `array`.

### Parameters

*   `array` **[Array][113]** The array to query.

### Examples

```javascript
initial([1, 2, 3]);
// => [1, 2]
```

Returns **[Array][113]** Returns the slice of `array`.

## isArray

Checks if `value` is classified as an `Array` object.

### Parameters

*   `value` **any** The value to check.

### Examples

```javascript
isArray([1, 2, 3]);
// => true

isArray(document.body.children);
// => false

isArray('abc');
// => false
```

Returns **[boolean][115]** Returns `true` if `value` is an array, else `false`.

## isMap

Checks if `value` is classified as a `Map` object.

### Parameters

*   `value` **any** The value to check.

### Examples

```javascript
isMap(new Map);
// => true

isMap(new WeakMap);
// => false
```

Returns **[boolean][115]** Returns `true` if `value` is map, else `false`.

## isNil

Checks if `value` is `null` or `undefined`.

### Parameters

*   `value` **any** The value to check.

### Examples

```javascript
isNil(null);
// => true

isNil(undefined);
// => true

isNil(NaN);
// => false
```

Returns **[boolean][115]** Returns `true` if `value` is nullish, else `false`.

## isNull

Check if `value` is `null`

### Parameters

*   `value` **any** The value to check.

### Examples

```javascript
isNull(null);
// => true

isNull(undefined);
// => false
```

Returns **[boolean][115]** Returns `true` if `value` is `null`, else `false`.

## isObjectLike

Checks if `value` is not `null` and has a `typeof` result of "object".

### Parameters

*   `value` **any** The value to check.

### Examples

```javascript
isObjectLike({});
// => true

isObjectLike([1, 2, 3]);
// => true

isObjectLike(() => {});
// => false

isObjectLike(null);
// => false
```

Returns **[boolean][115]** Returns `true` if `value` is object-like, else `false`.

## isString

Checks if `value` is classified as a `String` primitive or object.

### Parameters

*   `value` **any** The value to check.

### Examples

```javascript
isString('abc');
// => true

isString(1);
// => false
```

Returns **[boolean][115]** Returns `true` if `value` is a string, else `false`.

## isUndefined

Check if `value` is `undefined`

### Parameters

*   `value` **any** The value to check.

### Examples

```javascript
isUndefined(undefined);
// => true

isUndefined(null);
// => false
```

Returns **[boolean][115]** Returns `true` if `value` is `undefined`, else `false`.

## last

Gets the last element of array.

### Parameters

*   `array` **[Array][113]** 

### Examples

```javascript
last([1, 2, 3]);
// => 3
```

Returns **any** 

## lt

Checks if `value` is less than `other`.

### Parameters

*   `value` **any** The value to compare.
*   `other` **any** The other value to compare.

### Examples

```javascript
lt(1, 3);
// => true

lt(3, 3);
// => false

lt(3, 1);
// => false
```

Returns **[boolean][115]** Returns true if value is less than other, else false.

## max

Computes the maximum value of `array`. If `array` is empty or falsey, `undefined` is returned.

### Parameters

*   `array` **[Array][113]** The array to iterate over.

### Examples

```javascript
max([4, 2, 8, 6]);
// => 8

max([])
// => undefined
```

Returns **any** Returns the maximum value.

## mean

Computes the mean of the values in `array`.

### Parameters

*   `array` **[Array][113]** 

### Examples

```javascript
mean([4, 2, 8, 6]);
// => 5
```

Returns **[number][112]** Returns the mean.

## min

Computes the minimum value of `array`. If `array` is empty or falsey, `undefined` is returned.

### Parameters

*   `array` **[Array][113]** The array to iterate over.

### Examples

```javascript
min([4, 2, 8, 6]);
// => 2

min([])
// => undefined
```

Returns **any** Returns the minimum value.

## multiply

Multiply two numbers.

### Parameters

*   `multiplier` **[number][112]** 
*   `multiplicand` **[number][112]** 

### Examples

```javascript
multiply(6, 4);
// => 24
```

Returns **[number][112]** Returns the product

## noop

This function do nothing.

### Examples

```javascript
noop();
// => undefined
```

## nth

Gets the element at index `n` of `array`. If `n` is negative, the nth element from the end is returned.

### Parameters

*   `array` **[Array][113]** The array to query.
*   `index` **[number][112]** The index of the element to return. (optional, default `0`)

### Examples

```javascript
nth(['a', 'b', 'c', 'd'], 1);
// => b

nth(['a', 'b', 'c', 'd'], -2);
// => c
```

Returns **any** Returns the nth element of `array`.

## partition

Splits a collection into two by callback.

### Parameters

*   `collection` **([Array][113] | [object][116])** The collection to iterate over.
*   `predicate` **[Function][114]** The function invoked per iteration.

### Examples

```javascript
const users = [
  { 'name': 'ivan', 'age': 18 },
  { 'name': 'adam', 'age': 25 },
  { 'name': 'carl', 'age': 39 }
];

partition(users, user => user.age >= 21);
// => objects for [['adam, carl'], ['ivan']]
```

Returns **[Array][113]** Returns the array of grouped elements.

## reverse

Reverses `array` so that the first element becomes the last, the second element becomes the second to last, and so on.
**Note:** This method mutates `array` and is based on [Array#reverse][117].

### Parameters

*   `array` **[Array][113]** The array to modify.

### Examples

```javascript
reverse([1, 2, 3]);
// => true
```

Returns **[Array][113]** Returns `array`.

## size

Gets the size of collection.

### Parameters

*   `collection` **([Array][113] | [Object][116] | [string][118])** 

### Examples

```javascript
size([1, 2, 3]);
// => 3

size({ foo: 'bar', baz: false });
// => 2

size('cobbles');
// => 7
```

Returns **[number][112]** 

## stubArray

This method returns a new empty array.

### Examples

```javascript
stubArray();
// => []
```

Returns **[Array][113]** Returns the new empty array

## stubFalse

This method returns `false`.

### Examples

```javascript
stubFalse();
// => false
```

Returns **[boolean][115]** 

## stubObject

This method returns a new empty object.

### Examples

```javascript
stubObject();
// => {}
```

Returns **[Object][116]** Returns the new empty object

## stubString

This method returns an empty string.

### Examples

```javascript
stubString();
// => ''
```

Returns **[string][118]** Returns the empty string

## stubTrue

This method returns `true`.

### Examples

```javascript
stubTrue();
// => true
```

Returns **[boolean][115]** 

## subtract

Subtract two numbers.

### Parameters

*   `minuend` **[number][112]** 
*   `subtrahend` **[number][112]** 

### Examples

```javascript
subtract(6, 4);
// => 2
```

Returns **[number][112]** The difference

## sum

Computes the sum of the values in array.

### Parameters

*   `array` **[Array][113]** 

### Examples

```javascript
sum([4, 2, 8, 6]);
// => 20
```

Returns **[number][112]** The sum

## tail

Gets all but the first element of `array`.

### Parameters

*   `array` **[Array][113]** The array to query

### Examples

```javascript
tail([1, 2, 3]);
// => [2, 3]
```

Returns **[Array][113]** Returns the slice of `array`.

## uniq

Creates a duplicate-free version of an array.

### Parameters

*   `array` **[Array][113]** 

### Examples

```javascript
uniq([2, 1, 2]);
// => [2, 1]
```

Returns **[Array][113]** 

## upperFirst

Converts the first character of `string` to upper case.

### Parameters

*   `string` **[string][118]** The string to convert. (optional, default `''`)

### Examples

```javascript
upperFirst('fred');
// => 'Fred'

upperFirst('FRED');
// => 'FRED'
```

Returns **[string][118]** Returns the converted string.

[1]: #add

[2]: #parameters

[3]: #examples

[4]: #chunk

[5]: #parameters-1

[6]: #examples-1

[7]: #constant

[8]: #parameters-2

[9]: #examples-2

[10]: #defaultto

[11]: #parameters-3

[12]: #examples-3

[13]: #divide

[14]: #parameters-4

[15]: #examples-4

[16]: #drop

[17]: #parameters-5

[18]: #examples-5

[19]: #dropright

[20]: #parameters-6

[21]: #examples-6

[22]: #gt

[23]: #parameters-7

[24]: #examples-7

[25]: #head

[26]: #parameters-8

[27]: #examples-8

[28]: #identity

[29]: #parameters-9

[30]: #examples-9

[31]: #initial

[32]: #parameters-10

[33]: #examples-10

[34]: #isarray

[35]: #parameters-11

[36]: #examples-11

[37]: #ismap

[38]: #parameters-12

[39]: #examples-12

[40]: #isnil

[41]: #parameters-13

[42]: #examples-13

[43]: #isnull

[44]: #parameters-14

[45]: #examples-14

[46]: #isobjectlike

[47]: #parameters-15

[48]: #examples-15

[49]: #isstring

[50]: #parameters-16

[51]: #examples-16

[52]: #isundefined

[53]: #parameters-17

[54]: #examples-17

[55]: #last

[56]: #parameters-18

[57]: #examples-18

[58]: #lt

[59]: #parameters-19

[60]: #examples-19

[61]: #max

[62]: #parameters-20

[63]: #examples-20

[64]: #mean

[65]: #parameters-21

[66]: #examples-21

[67]: #min

[68]: #parameters-22

[69]: #examples-22

[70]: #multiply

[71]: #parameters-23

[72]: #examples-23

[73]: #noop

[74]: #examples-24

[75]: #nth

[76]: #parameters-24

[77]: #examples-25

[78]: #partition

[79]: #parameters-25

[80]: #examples-26

[81]: #reverse

[82]: #parameters-26

[83]: #examples-27

[84]: #size

[85]: #parameters-27

[86]: #examples-28

[87]: #stubarray

[88]: #examples-29

[89]: #stubfalse

[90]: #examples-30

[91]: #stubobject

[92]: #examples-31

[93]: #stubstring

[94]: #examples-32

[95]: #stubtrue

[96]: #examples-33

[97]: #subtract

[98]: #parameters-28

[99]: #examples-34

[100]: #sum

[101]: #parameters-29

[102]: #examples-35

[103]: #tail

[104]: #parameters-30

[105]: #examples-36

[106]: #uniq

[107]: #parameters-31

[108]: #examples-37

[109]: #upperfirst

[110]: #parameters-32

[111]: #examples-38

[112]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number

[113]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array

[114]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function

[115]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean

[116]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object

[117]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reverse

[118]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String
