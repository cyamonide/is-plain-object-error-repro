<p align="center">
  <h3 align="center"></h3>

  <p align="center">
      🐛 Reproduction case for the issue on octokit/rest.js is-plain-object problem 🐛 <br/>
      The issue can be found <a href="https://github.com/octokit/rest.js/issues/1929">here</a>
    <br />
  </p>
</p>

### How to use?

```bash
git clone git@github.com:gagoar/is-plain-object-error-repro.git
nvm use
npm install
npm run all
```

You should see an error when executing the compiled binary much like this:

```javascript
is-plain-object-error-repro/dist/index.js:358
    if (isPlainObject.isPlainObject(options[key])) {
                      ^

TypeError: isPlainObject.isPlainObject is not a function
    at Object.keys.forEach.key (/Users/gfrigerio/base/is-plain-object-error-repro/dist/index.js:358:23)
    at Array.forEach (<anonymous>)
    at mergeDeep (/Users/gfrigerio/base/is-plain-object-error-repro/dist/index.js:357:24)
    at merge (/Users/gfrigerio/base/is-plain-object-error-repro/dist/index.js:399:25)
    at withDefaults (/Users/gfrigerio/base/is-plain-object-error-repro/dist/index.js:695:20)
    at Object.385 (/Users/gfrigerio/base/is-plain-object-error-repro/dist/index.js:723:18)
    at __webpack_require__ (/Users/gfrigerio/base/is-plain-object-error-repro/dist/index.js:24:31)
    at Object.753 (/Users/gfrigerio/base/is-plain-object-error-repro/dist/index.js:2831:16)
    at __webpack_require__ (/Users/gfrigerio/base/is-plain-object-error-repro/dist/index.js:24:31)
    at Object.448 (/Users/gfrigerio/base/is-plain-object-error-repro/dist/index.js:748:15)
```

The code used is the same shared as an example in the [Readme](https://github.com/octokit/rest.js/blob/master/README.md) on the library itself.
