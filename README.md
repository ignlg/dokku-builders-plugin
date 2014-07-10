# dokku-builders

Plugin for [dokku][dokku] to run tools and package managers on build/release.

Supported tools:
* [npm][npm] (update)
* [bower][bower]
* [grunt][grunt]
* [gulp][gulp]

## Installation

On your _dokku_ server:
```sh
git clone https://github.com/ignlg/dokku-builders-plugin.git /var/lib/dokku/plugins/builders
```

## Config file

You can change the behavior with a `.dokkubuild` config file in your project's root folder or assigning environment variables.

`.dokkubuild` example at: https://github.com/ignlg/dokku-builders-plugin/blob/master/.dokkubuild

### Defaults
```sh
BUILD_NPM_UPDATE=0
BUILD_BOWER=1
BUILD_BOWER_PRUNE=1
BUILD_BOWER_INSTALL=1
BUILD_BOWER_UPDATE=0
BUILD_BOWER_CACHE=1
BUILD_BOWER_COMPONENTS="bower_components"
BUILD_GRUNT=1
BUILD_GULP=1
```

## Inspired by
https://github.com/thrashr888/dokku-bower-grunt-build-plugin
https://github.com/firstandthird/dokku-buildui
https://github.com/AntJanus/dokku-bower-install

## License

The MIT License (MIT)

Copyright (c) 2014 Ignacio Lago

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

[dokku]: https://github.com/progrium/dokku
[npm]: https://www.npmjs.org/
[bower]: http://bower.io/
[grunt]: http://gruntjs.com/
[gulp]: http://gulpjs.com/