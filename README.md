# dokku-builders

Plugin for [dokku][dokku] to run tools and package managers on build/release.

Supported tools:
* [bower][bower]
* [compass][compass]
* [grunt][grunt]
* [gulp][gulp]
* [npm][npm]

## Installation

```shell
# on dokku 0.3.x
cd /var/lib/dokku/plugins
git clone https://github.com/ignlg/dokku-builders-plugin.git builders
dokku plugins-install

# on dokku 0.4.x
dokku plugin:install https://github.com/ignlg/dokku-builders-plugin.git builders
```

## Config file: `.builders`

You can change the behavior with a `.builders` config file in your project's root folder or assigning environment variables.

All the options are boolean with value `0` or `1`.

#### Example
```shell
BUILD_BOWER=1
BUILD_COMPASS=1
BUILD_GULP=1
```
Full `.builders` example at: https://github.com/ignlg/dokku-builders-plugin/blob/master/.builders

#### Basic
- `BUILD_BOWER` Default: `0`.

	> Enables Bower.

- `BUILD_COMPASS` Default: `0`.

	> Enables Compass via Bundler.

- `BUILD_GRUNT` Default: `0`.

	> Enables Grunt.

- `BUILD_GULP` Default: `0`.

	> Enables Gulp.

#### Advanced
- `BUILD_NPM_UPDATE` Default: `0`.

	> Forces npm update.

- `BUILD_BOWER_PRUNE` Default: `0`.

	> Forces bower prune of unused cached packages.

- `BUILD_BOWER_INSTALL` Default: `1`.

	> Bower install.

- `BUILD_BOWER_UPDATE` Default: `1`.

	> Bower update.

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

### Thanks to
* https://github.com/thrashr888/dokku-bower-grunt-build-plugin
* https://github.com/firstandthird/dokku-buildui
* https://github.com/AntJanus/dokku-bower-install

[dokku]: http://progrium.viewdocs.io/dokku/
[npm]: https://www.npmjs.org/
[bower]: http://bower.io/
[grunt]: http://gruntjs.com/
[gulp]: http://gulpjs.com/
[compass]: http://compass-style.org/
