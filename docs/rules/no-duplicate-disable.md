# disallows duplicate `eslint-disable` comments (eslint-comments/no-duplicate-disable)

Duplicate of `eslint-disable` directive-comments implies that there is a mix of wide-range directive-comments and narrow-range directive-comments.
The mix may cause to overlook ESLint warnings in future.

This rule warns duplicate `eslint-disable` directive-comments.

## Rule Details

Examples of :-1: **incorrect** code for this rule:

```js
/*eslint eslint-comments/no-duplicate-disable: error */

/*eslint-disable no-undef */

var foo = bar() //eslint-disable-line no-undef
```

```js
/*eslint eslint-comments/no-duplicate-disable: error */

/*eslint-disable*/

var foo = bar() //eslint-disable-line no-undef
```

Examples of :+1: **correct** code for this rule:

```js
/*eslint eslint-comments/no-duplicate-disable: error */

/*eslint-disable no-undef */

var foo = bar()
```

```js
/*eslint eslint-comments/no-duplicate-disable: error */

var foo = bar() //eslint-disable-line no-undef
```
