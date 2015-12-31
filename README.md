# mongodb-proxy-memcache

> A memory cache implementation for mongodb-proxy

## Install

Install with [npm](https://www.npmjs.com/)

```sh
$ npm install mongodb-proxy-memcache --save
```

### Usage

```js
var proxy = require('mongodb-proxy');
var MemCache = require('mongodb-proxy-memcache');

var options = {
    name: 'Northwind',
    host: 'localhost',
    port: 27017,
	credentials: {
		user: 'user',
		password: 'password'
	}
};

var db = proxy.create(options);

db.configure(function (config) {
    config.cache(new MemCache());
});
```
## license

	The MIT License (MIT)

	Copyright (c) 2014 akon

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
