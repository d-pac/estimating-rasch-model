 [![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Dependency Status][daviddm-url]][daviddm-image]

# Conditional estimation of Rasch model

`estimate()` estimates the parameters of the Rasch/Bradley-Terry_Luce model with a conditional maximum likelihood procedure.
This is an iterative procedure using Newton's method of optimization.
The algorithm concept was initially developed by Rasch (1960) and implemented by Pollitt (2012) and [NoMoreMarking ltd.](https://github.com/NoMoreMarking/cj) among others.

Our module was originally based on the code of [NoMoreMarking ltd.](https://github.com/NoMoreMarking/cj) and has been further optimised.

## Tests

You can run the unit tests with

```
$ yarn test
```

[npm-url]: https://npmjs.org/package/estimating-rasch-model

[npm-image]: https://badge.fury.io/js/estimating-rasch-model.svg

[travis-url]: https://travis-ci.org/d-pac/estimating-rasch-model

[travis-image]: https://travis-ci.org/d-pac/estimating-rasch-model.svg?branch=master

[daviddm-url]: https://david-dm.org/d-pac/estimating-rasch-model.svg?theme=shields.io

[daviddm-image]: https://david-dm.org/d-pac/estimating-rasch-model

## API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### Item

Type: [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)

**Properties**

-   `id` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** ID of the item
-   `ranked` **[boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** whether or not the item is ranked. Only unranked items (i.e. ranked: `false`) are estimated
-   `ability` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** the ability
-   `se` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** standard error

### Comparison

Type: [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)

**Properties**

-   `itemA` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** the ID of the "A" item
-   `itemB` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** the ID of the "B" item
-   `selected` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)?** the ID of the selected item

### ValueObject

Type: [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)

**Properties**

-   `id` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** the ID of the corresponding item
-   `selectedNum` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** the number of times the item has been selected
-   `comparisonNum` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** the number of times the item has been compared
-   `ranked` **[boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** whether or not the item is ranked. Only unranked items (i.e. ranked: `false`) are estimated
-   `ability` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)??** the ability
-   `se` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)??** standard error

### estimate

Estimates the items featured in comparisons

**Parameters**

-   `comparisons` **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Comparison](#comparison)>** 
-   `items` **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Item](#item)>** 

Returns **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[ValueObject](#valueobject)>** 
