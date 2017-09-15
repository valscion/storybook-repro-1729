Reproduction repository for https://github.com/storybooks/storybook/issues/1729

```
npm install
npm run storybook
```

...and behold, you'll get this error:

```
npm run storybook

> storybook-repro-1729@0.1.0 storybook /projects/storybook-repro-1729
> start-storybook -p 9009 -s public

module.js:457
    throw err;
    ^

Error: Cannot find module 'babel-plugin-transform-regenerator'
    at Function.Module._resolveFilename (module.js:455:15)
    at Function.resolve (internal/module.js:27:19)
    at Object.<anonymous> (/projects/storybook-repro-1729/node_modules/@storybook/react/dist/server/config/babel.js:12:21)
    at Module._compile (module.js:556:32)
    at Object.Module._extensions..js (module.js:565:10)
    at Module.load (module.js:473:32)
    at tryModuleLoad (module.js:432:12)
    at Function.Module._load (module.js:424:3)
    at Module.require (module.js:483:17)
    at require (internal/module.js:20:19)
```

Steps taken in this repository

```
nvm use v6.4.0
npm i -g npm@2.x
npm i -g create-react-app
create-react-app .
npm i -g @storybook/cli
getstorybook --use-npm
# Modify package.json to pin version of @storybook/xyz packages
```


