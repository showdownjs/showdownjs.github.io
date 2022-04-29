«««
title: Annoucement: Showdown 2.1.0 released,
author: Estevão Soares dos Santos,
author_avatar: img/avatars/tivie.jpg,
date: 2022-04-21,
language: en,
image: img/blog/2018.10.16.jpg,
summary: We are very happy to announce the release of version 2.1.0 which fixes some bugs and security issues
»»»

Release 2.1.0 comprises a complete refactor of the CLI tool. There are only a few changes beyond 1.9.1 as noted below. 
The major driver of this update is to remove the yargs dependency, switching to commander, a more lightweight (and no-dependecies)
library.

Also, the license changed from BSD-3-Clause to MIT

The changes relative to version 1.9.x are as follow:

### Breaking Changes
* Supported Node Versions were set to match the [node release schedule](https://nodejs.org/en/about/releases/) which at
  the time of writing includes Node 12.x, 14.x, 16.x and 17.x
* The `yargs` dependency was removed.
* The Showdown license has been changed from BSD-3-Clause to MIT
* The CLI no longer accepts "extra options". Instead you should pass the `-c` flag. To update:

    before:
    ```
    showdown makehtml -i foo.md -o bar.html --strikethrough --emoji
    ```

    after:
    ```
    showdown makehtml -i foo.md -o bar.html -c strikethrough -c emoji
    ```

### Bug Fixes

* allow escaping of colons ([25c4420](https://github.com/showdownjs/showdown/commit/25c4420))
* reduce npm package size  ([35730b7](https://github.com/showdownjs/showdown/commit/35730b7)), closes [#619](https://github.com/showdownjs/showdown/issues/619)

### Features

* Added `ellipsis` option to configure if the ellipsis unicode character is used or not. ( Thanks @VladimirV99 )
* Added a default security policy. Please report security issues to the issues tab on GitHub.


You can download/use the [new version here.](https://github.com/showdownjs/showdown/releases)
