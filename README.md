# Splearch

[![Greenkeeper badge](https://badges.greenkeeper.io/Qard/splearch.svg)](https://greenkeeper.io/)
Splearch provides a simplified abstraction of regex searching to locate patterns in a string. It works very similar to how Dir.glob does in ruby in that * matches word characters, ** matches all characters, and braces can be used to expand lists to multiple matching possibilities. It simply builds and returns a RegExp object, which you can use however you see fit.

## Install

    npm install splearch

## Usage

    var regex = Splearch('foo.{bar**,baz{1..5}}.buz')
    regex.test('foo.bart.simpson.buz') // true
    regex.test('foo.baz3.buz') // true

    // You can also disable specific features
    Splearch('foo.*.bux', {
      braces: false // Can be broken down to 'ranges' and 'lists'
      , double_splats: false
    })

---

### Copyright (c) 2011 Stephen Belanger
#### Licensed under MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.