gulp-bem-bundler-merged
=======================

*DEPRECATED repository, moved to mono repository [gulp-bem](https://github.com/bem/gulp-bem/tree/master/packages/gulp-bem-bundler-merged)*

Install
-------

```
$ npm install --save-dev gulp-bem-bundler-merged
```

Usage
-----

```js
const bundler = require('gulp-bem-bundler-fs');
const mergedBundler = require('gulp-bem-bundler-merged');

bundler('*.bundles/*')
    .pipe(mergedBundler({
        name: 'common',
        path: './*.bundles/common'
    }))
    .on('data', data => {
        console.log(data.name);
        console.log(data.decl);
    });
// common
// [ {block: 'a'}, {block: 'b'}, {block: 'c'}, ... ]
```
