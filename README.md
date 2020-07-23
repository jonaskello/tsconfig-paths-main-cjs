# How to install and run

Install:

```
yarn
```

This works (without tsconfig-paths loaded):

```
yarn start
```

This does not work (with tsconfig-paths loaded):

```
yarn start-paths
```

# Ouput

```
$ node --version
v12.14.1

$ yarn start
yarn run v1.21.1
$ tsc && node ./lib/main.js
Engage!

  Beets are red,
  Plums are blue,
  Colorette!.

Done in 0.54s.

$ yarn start-paths
yarn run v1.21.1
$ tsc && node -r tsconfig-paths/register ./lib/main.js
/home/jonkel/code/github/jonaskello/tsconfig-paths-main-cjs/node_modules/colorette/index.js:28
export const options = Object.defineProperty({}, "enabled", {
^^^^^^

SyntaxError: Unexpected token 'export'
    at Module._compile (internal/modules/cjs/loader.js:891:18)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:991:10)
    at Module.load (internal/modules/cjs/loader.js:811:32)
    at Function.Module._load (internal/modules/cjs/loader.js:723:14)
    at Module.require (internal/modules/cjs/loader.js:848:19)
    at require (internal/modules/cjs/helpers.js:74:18)
    at Object.<anonymous> (/home/jonkel/code/github/jonaskello/tsconfig-paths-main-cjs/lib/main.js:3:19)
    at Module._compile (internal/modules/cjs/loader.js:955:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:991:10)
    at Module.load (internal/modules/cjs/loader.js:811:32)
error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```
