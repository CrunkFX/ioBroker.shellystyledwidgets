![Logo](admin/shellystyledwidgets.png)
# ioBroker.shellystyledwidgets

[![NPM version](http://img.shields.io/npm/v/iobroker.shellystyledwidgets.svg)](https://www.npmjs.com/package/iobroker.shellystyledwidgets)
[![Downloads](https://img.shields.io/npm/dm/iobroker.shellystyledwidgets.svg)](https://www.npmjs.com/package/iobroker.shellystyledwidgets)
![Number of Installations (latest)](http://iobroker.live/badges/shellystyledwidgets-installed.svg)
![Number of Installations (stable)](http://iobroker.live/badges/shellystyledwidgets-stable.svg)
[![Dependency Status](https://img.shields.io/david/CrunkFX/iobroker.shellystyledwidgets.svg)](https://david-dm.org/CrunkFX/iobroker.shellystyledwidgets)
[![Known Vulnerabilities](https://snyk.io/test/github/CrunkFX/ioBroker.shellystyledwidgets/badge.svg)](https://snyk.io/test/github/CrunkFX/ioBroker.shellystyledwidgets)

[![NPM](https://nodei.co/npm/iobroker.shellystyledwidgets.png?downloads=true)](https://nodei.co/npm/iobroker.shellystyledwidgets/)

**Tests:** ![Test and Release](https://github.com/CrunkFX/ioBroker.shellystyledwidgets/workflows/Test%20and%20Release/badge.svg)

## shellystyledwidgets adapter for ioBroker

A set of Widgets based on Allterco´s Shelly Widgets

## Developer manual
This section is intended for the developer. It can be deleted later

### Getting started

You are almost done, only a few steps left:
1. Create a new repository on GitHub with the name `ioBroker.shellystyledwidgets`
1. Initialize the current folder as a new git repository:  
    ```bash
    git init
    git add .
    git commit -m "Initial commit"
    ```
1. Link your local repository with the one on GitHub:  
    ```bash
    git remote add origin https://github.com/CrunkFX/ioBroker.shellystyledwidgets
    ```

1. Push all files to the GitHub repo:  
    ```bash
    git push origin master
    ```

1. Head over to [widgets/shellystyledwidgets.html](widgets/shellystyledwidgets.html) and start programming!

### Best Practices
We've collected some [best practices](https://github.com/ioBroker/ioBroker.repositories#development-and-coding-best-practices) regarding ioBroker development and coding in general. If you're new to ioBroker or Node.js, you should
check them out. If you're already experienced, you should also take a look at them - you might learn something new :)

### Scripts in `package.json`
Several npm scripts are predefined for your convenience. You can run them using `npm run <scriptname>`
| Script name | Description |
|-------------|-------------|
| `test:package` | Ensures your `package.json` and `io-package.json` are valid. |
| `test` | Performs a minimal test run on package files. |

### Publishing the widget
Since you have chosen GitHub Actions as your CI service, you can 
enable automatic releases on npm whenever you push a new git tag that matches the form 
`v<major>.<minor>.<patch>`. The necessary steps are described in `.github/workflows/test-and-release.yml`.

To get your widget released in ioBroker, please refer to the documentation 
of [ioBroker.repositories](https://github.com/ioBroker/ioBroker.repositories#requirements-for-adapter-to-get-added-to-the-latest-repository).

### Test the adapter manually on a local ioBroker installation
In order to install the adapter locally without publishing, the following steps are recommended:
1. Create a tarball from your dev directory:  
    ```bash
    npm pack
    ```
1. Upload the resulting file to your ioBroker host
1. Install it locally (The paths are different on Windows):
    ```bash
    cd /opt/iobroker
    npm i /path/to/tarball.tgz
    ```

For later updates, the above procedure is not necessary. Just do the following:
1. Overwrite the changed files in the adapter directory (`/opt/iobroker/node_modules/iobroker.shellystyledwidgets`)
1. Execute `iobroker upload shellystyledwidgets` on the ioBroker host

## Changelog

### 0.0.1
* (CrunkFX) initial release

## License
MIT License

Copyright (c) 2021 CrunkFX <crunk.sfx@gmail.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.