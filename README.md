# Eslint + Standard.js - Vue.js Configuation
This repository provides a boilerplate setup for linting Vue.js applications with the Standard.js code style It includes a package.json file and an .eslintrc configuration file, pre-configured to use Standard.js, a popular JavaScript code style and linter.


## Usage
- Simply copy the package.json dependcies and then run 
`npm install`
- Create a .eslint.cjs and copy over the content
- Enjoy!

# Manual Installations


**Install the packages below to get ESlint configured to Standard.js in a Vue.js Application**
* Standard,js: [npm](https://www.npmjs.com/package/standard)\
`$ npm install standard --save-dev`

* ESLint Standard.js Config: [npm](https://www.npmjs.com/package/eslint-config-standard)\
`npm install eslint-config-standard`

* ESLint Vue.js: [docs](https://eslint.vuejs.org/user-guide/)\
`npm install --save-dev eslint eslint-plugin-vue`



# Config Setup 

**Make a file in the root of the directory named `.eslintrc.cjs` and inside this file paste the following code:**

```
/* eslint-env node */
module.exports = {
  root: true,
  extends: [
    'plugin:vue/vue3-essential',
    'plugin:vue/recommended',
    'standard'
  ],
  parserOptions: {
    ecmaVersion: 'latest'
  }
}
```

This file will config ESLint to Standard.js rules in your Vue.js application

# Running

**If you need to, you can add this line of code into your `package.json` scripts section to add the run lint script**

``` {
  ...
  "scripts": {
    "lint": "eslint . --ext .vue,.js,.jsx,.cjs,.mjs --fix --ignore-path .gitignore",
  },
  ...
```
`npm run lint` now runs the Standard.js configurated ESLint



