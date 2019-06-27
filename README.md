# no-used-export

[![Dependency Status](https://david-dm.org/plantain-00/no-unused-export.svg)](https://david-dm.org/plantain-00/no-unused-export)
[![devDependency Status](https://david-dm.org/plantain-00/no-unused-export/dev-status.svg)](https://david-dm.org/plantain-00/no-unused-export#info=devDependencies)
[![Build Status: Linux](https://travis-ci.org/plantain-00/no-unused-export.svg?branch=master)](https://travis-ci.org/plantain-00/no-unused-export)
[![Build Status: Windows](https://ci.appveyor.com/api/projects/status/github/plantain-00/no-unused-export?branch=master&svg=true)](https://ci.appveyor.com/project/plantain-00/no-unused-export/branch/master)
[![npm version](https://badge.fury.io/js/no-unused-export.svg)](https://badge.fury.io/js/no-unused-export)
[![Downloads](https://img.shields.io/npm/dm/no-unused-export.svg)](https://www.npmjs.com/package/no-unused-export)
[![type-coverage](https://img.shields.io/badge/dynamic/json.svg?label=type-coverage&prefix=%E2%89%A5&suffix=%&query=$.typeCoverage.atLeast&uri=https%3A%2F%2Fraw.githubusercontent.com%2Fplantain-00%2Fno-used-export%2Fmaster%2Fpackage.json)](https://github.com/plantain-00/no-used-export)

A CLI tool to check whether exported things in a module is used by other modules.

## install

`yarn global add no-unused-export`

## features

+ check whether exported variable, function, type, class, interface in a module is used by other modules
+ check whether public members of class are used outside of the class
+ check whether less or scss variables are used
+ check whether template use non-public members for angular
+ check whether `key` exist for `v-for` and `trackBy` exists for `*ngFor`
+ check whether module `import`ed in source code is also in `dependencies` or `peerDependencies` of `package.json`(enabled by `--strict`)
+ check whether module in `dependencies` or `peerDependencies` of `package.json` is also `import`ed in source code (enabled by `--strict`)

## usage

`no-unused-export "src/*.ts"`

### exclude source files

`no-unused-export "src/*.ts" --exclude "src/*.d.ts"`

`--exclude` is repeatable

### exclude `export`s

```ts
/**
 * @public
 */
export const foo = 1;
```
