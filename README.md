# Contributing to TypedAPIs

Welcome, and thanks for contributing to the TypedAPIs organization. Our goal is to establish basic API types for all APIs, and start with APIs that are not available as wrappers in both sync and async flavors of Python. 

## Repository structure

Every major version of an API should get it's own repository in order to allow types for multiple API versions to co-exist. If you need to make a new repository, it is recommended to use the [template repository](https://github.com/TypedAPIs/template) to do so, as it already contains a lot of the boilerplate code.

### Changing the template

The template has two placeholders, `example-site` and `website-name`. These placeholders should be replaced with the appropriate values.

_Tip: It is recommended to use an IDE with a project-wide find-and-replace tool, such as the [IntelliJ suite of IDEs](https://www.jetbrains.com/idea/) or [VSCode](https://code.visualstudio.com/)._

* `website-name` is the domain name of the API website, or another known identifier. For example, if I am building a type system for the version 2 MyAnimeList API, I would replace all instances of `website-name` with `myanimelist.net v2`.
* `example-site` is the package name of the API types, as periods cannot be in package names for Python or npm. For example, if I am building a type system for the version 2 MyAnimeList API, I would replace all instances of `example-site` with `myanimelist-v2`.

## General Documentation

Every endpoint should get their own file. Each endpoint should get a type object characterizing the overall structure of the document. Every JSON object with constant keys should get an interface object.

## Python Documentation

If the API has multiple endpoints under a single category (such as oauth, admin, etc.), they should go in their own package. Sphinx documentation should aim to replicate the structure of the Python documentation, including these categories.

### Glossary

Some APIs use terms over and over again that mean a specific term but are not specialized enough for their own type, such as a special type of string. One example includes snowflakes from the Discord API, and while these are integers they also have some specialized meaning. These types should be defined in the `glossary.rst` file.
