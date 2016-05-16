# ![Typings](https://cdn.rawgit.com/typings/typings/master/logo.svg)

[![NPM version][npm-image]][npm-url]
[![NPM downloads][downloads-image]][downloads-url]
[![Build status][travis-image]][travis-url]
[![Gitter][gitter-image]][gitter-url]

> The TypeScript Definition Manager.

**Updating from `0.x` to `1.0`?** Make sure you `rm -rf typings/`, re-install, and update `tsconfig.json`. See [the release](https://github.com/typings/typings/releases/tag/v1.0.0) for more information!

## Quick Start

```sh
# Install Typings CLI utility.
npm install typings --global

# Search for definitions.
typings search tape

# Find an available definition (by name).
typings search --name react

# If you use the package as a module:
# Install non-global typings (defaults to "npm" source, configurable through `defaultSource` in `.typingsrc`)
typings install chai --save

# If you use the package through script tag, or
# it is part of the environment, or
# the non-global typings is not yet available:
typings install mocha --global --save

# Install typings from particular registry
typings install env~atom --global --save
typings install npm~bluebird --save

# Use `typings/index.d.ts` (in `tsconfig.json` or as a `///` reference).
cat typings/index.d.ts
```

## Usage

**Typings** is the simple way to manage and install TypeScript definitions. It uses `typings.json`, which can resolve to the Typings Registry, GitHub, NPM, Bower, HTTP and local files. Packages can use type definitions from various sources and different versions, knowing they will _never_ conflict for users.

```sh
typings install debug --save
```

The [public registry](https://github.com/typings/registry) is maintained by the community, and is used to resolve official type definitions for JavaScript packages.

## Read More

* [Commands](docs/commands.md)
* [Coming from TSD?](docs/tsd.md)
* [Example typings](docs/examples.md)
* [Why external modules?](docs/external-modules.md)
* [About the registry](docs/registry.md)
* [FAQ](docs/faq.md)

## Sources

* `npm` - dependencies from [NPM](http://npmjs.org/)
* `github` - dependencies directly from [GitHub](https://github.com/) (E.g. [Duo](http://duojs.org/), [JSPM](http://jspm.io/))
* `bower` - dependencies from [Bower](http://bower.io/)
* `common` - "standard" libraries without a known "source"
* `shared` - shared library functionality
* `lib` - shared environment functionality (mirror of `shared`) (`--global`)
* `env` - environments (E.g. `atom`, `electron`) (`--global`)
* `global` - global (`window.<var>`) libraries (`--global`)
* `dt` - typings from [DefinitelyTyped](https://github.com/DefinitelyTyped/DefinitelyTyped) (usually `--global`)

## Contributing

```sh
# Installation
# Fork this repo (https://github.com/typings/typings)
# Clone the fork (E.g. `https://github.com/<your_username>/typings.git`)
cd typings

# Install modules
npm install

# Build
npm run build

# Test
npm run test
```

## [Change Log](https://github.com/typings/typings/releases)

## License

MIT

[npm-image]: https://img.shields.io/npm/v/typings.svg?style=flat
[npm-url]: https://npmjs.org/package/typings
[downloads-image]: https://img.shields.io/npm/dm/typings.svg?style=flat
[downloads-url]: https://npmjs.org/package/typings
[travis-image]: https://img.shields.io/travis/typings/typings.svg?style=flat
[travis-url]: https://travis-ci.org/typings/typings
[gitter-image]: https://badges.gitter.im/typings/typings.svg
[gitter-url]: https://gitter.im/typings/typings?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge
