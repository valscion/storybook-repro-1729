Reproduction repository for https://github.com/storybooks/storybook/issues/1729

This is the branch that is fixed, see comparison here: https://github.com/valscion/storybook-repro-1729/pull/1

```
npm install
npm run storybook
```

Important tidbit is in commit 755e360c13a76cbf7a3dbe0e0f15716e385613de:

```
commit 755e360c13a76cbf7a3dbe0e0f15716e385613de
Author: Vesa Laakso <laakso.vesa@gmail.com>
Date:   Fri Sep 15 11:26:10 2017 +0300

    Add a binary package of @storybook/react package

    This tarball is the result of running `npm pack` in this commit:
    https://github.com/valscion/storybook/commit/64e2f6b188adb7377a5d2e18e213ba44d3c4d181

    I would've gone with a git URL in package.json, if only npm would
    support monorepos, but no.
```
