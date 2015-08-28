[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)

# rb-conventional-changelog

![git cz](http://i.imgur.com/D6lFxHQ.gif)

## Setup

Install commitizen

```
npm install -g commitizen
```

Install the `rb-conventional-changelog` package.

```
npm install --save-dev rb-conventional-changelog
```

Create a `.cz.json` file with the following content:

```
{
  "path": "node_modules/rb-conventional-changelog/"
}
```

## Usage

```
git cz
```

#### Examples

```
feat: add 'graphiteWidth' option
```

```
fix: stop graphite breaking when width < 0.1
```

```
perf: remove graphiteWidth option

BREAKING CHANGE: The graphiteWidth option has been removed. The default graphite width of 10mm is always used for performance reason.

Closes https://github.com/angular/angular/issues/3826
```

### Commit Message Format

* A commit message consists of a **header**, **body** and **footer**.  
* The header has a **type** and a **subject**:

```
{{type}}: {{subject}}
<BLANK LINE>
{{body}}
<BLANK LINE>
{{breaking changes}}
<BLANK LINE>
{{footer}}
```

The **header** is mandatory and the **scope** of the header is optional.

Any line of the commit message cannot be longer 100 characters! This allows the message to be easier
to read on GitHub as well as in various git tools.

### Type

Must be one of the following:

* `feat`: A new feature.
* `fix`: A bug fix.
* `docs`: Documentation only changes.
* `style`: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc).
* `refactor`: A code change that neither fixes a bug or adds a feature.
* `perf`: A code change that improves performance.
* `test`: Adding missing tests.
* `chore`: Changes to the build process (`grunt`) or auxiliary tools and libraries such as documentation generation and linters (`jshint`, etc.)

### Subject

The subject contains succinct description of the change:

* Use the imperative, present tense: "change" not "changed" nor "changes"
* Don't capitalize first letter
* No dot (.) at the end.

### Body

Just as in the **subject**, use the imperative, present tense: "change" not "changed" nor "changes".
The body should include the motivation for the change and contrast this with previous behavior.

### Breaking Changes

**Breaking Changes** should start with the word `BREAKING CHANGE:` with a space or two newlines.

### Footer

The footer is the place to reference any tasks that this commit **Closes**.
