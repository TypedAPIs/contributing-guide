# Contributing to TypedAPIs

Welcome, and thanks for contributing to the TypedAPIs organization. Our goal is to establish basic API types for all APIs, and start with APIs that are not available as wrappers in both sync and async flavors of Python. 

## Repository structure

Every major version of an API should get it's own repository in order to allow types for multiple API versions to co-exist. If you need to make a new repository, it is recommended to use the [template repository](https://github.com/TypedAPIs/template) to do so, as it already contains a lot of the boilerplate code.

### Changing the template

The template has two placeholders, `example-site` and `website-name`.

* `website-name` is the domain name of the API website, or another known identifier. For example, if I am building a type system for the version 2 MyAnimeList API, I would replace all instances of `website-name` with `myanimelist.net v2`.
* `example-site` is the package name of the API types, as periods cannot be in package names for Python or npm. For example, if I am building a type system for the version 2 MyAnimeList API, I would replace all instances of `example-site` with `myanimelist-v2`.
