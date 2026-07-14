# jasonbhill.com

This is the repo that backs my website.

### Hugo and Anatole

The site lives in `jasonbhill.com/` and is built with [Hugo](https://gohugo.io/) using the [Anatole](https://github.com/lxndrblz/anatole) theme, installed as a git submodule at `jasonbhill.com/themes/anatole`.

#### Prerequisites

- [Hugo](https://gohugo.io/installation/) (extended edition)
- [Dart Sass](https://sass-lang.com/dart-sass/), required by the theme for compiling SCSS. On macOS: `brew install dart-sass && ln -s "$(brew --prefix dart-sass)/bin/sass" "$(brew --prefix dart-sass)/bin/dart-sass"` (Hugo looks for a binary literally named `dart-sass` on your `PATH`).

#### Getting started

Clone the repo with submodules (or run `git submodule update --init --recursive` afterwards):

```bash
git clone --recurse-submodules <repo-url>
cd jasonbhill.com/jasonbhill.com
```

Run the local dev server:

```bash
hugo server
```

Build the static site (output goes to `jasonbhill.com/jasonbhill.com/public/`):

```bash
hugo
```

#### Updating the theme

```bash
cd jasonbhill.com/themes/anatole
git fetch --tags
git checkout <tag>
cd -
git add jasonbhill.com/themes/anatole
git commit -m "Update Anatole theme to <tag>"
```
