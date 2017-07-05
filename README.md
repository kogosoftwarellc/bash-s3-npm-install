# s3-npm-install
> Install node_modules/ from s3.

## Overview

`npm install` is likely one of the longest running steps in any build.  This script
aims to reduce that by storing `node_modules` in s3.  How can that work?

With `npm@v5.0` we now have `package-lock.json`.  If this file doesn't change, then
the `node_modules` directory can be tarballed up and stored in s3 for later
retrieval.

## Requirements

* `package-lock.json` checked into your project.
* `aws` available on your path and configured to use `aws s3`
* `npm@>=5`
* `md5sum` will be used to compare `package-lock.json` against the tarballname in s3

## Usage

See `s3-npm-install -h`

## LICENSE
``````
The MIT License (MIT)

Copyright (c) 2017 Kogo Software LLC

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
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
``````
