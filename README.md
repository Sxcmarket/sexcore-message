# Sexcoin Message Verification and Signing for Sexcore


[![NPM Package](https://img.shields.io/npm/v/sexcore-message.svg?style=flat-square)](https://www.npmjs.org/package/sexcore-message)
[![Build Status](https://travis-ci.org/Sxcmarket/sexcore-message.svg?branch=master)](https://travis-ci.org/Sxcmarket/sexcore-message)
[![Coverage Status](https://coveralls.io/repos/github/Sxcmarket/sexcore-message/badge.svg?branch=master)](https://coveralls.io/github/Sxcmarket/sexcore-message?branch=master)

sexcore-message adds support for verifying and signing sexcoin messages in [Node.js](http://nodejs.org/) and web browsers.

See [the main sexcore repo](https://github.com/sxcmarket/sexcore) for more information.

## Getting Started

```sh
npm install sexcore-message
```

```sh
bower install sexcore-message
```

To sign a message:

```javascript
var sexcore = require('sexcore-lib');
var Message = require('sexcore-message');

var privateKey = litecore.PrivateKey.fromWIF('cPBn5A4ikZvBTQ8D7NnvHZYCAxzDZ5Z2TSGW2LkyPiLxqYaJPBW4');
var signature = Message('hello, world').sign(privateKey);
```

To verify a message:

```javascript
var address = 'n1ZCYg9YXtB5XCZazLxSmPDa8iwJRZHhGx';
var signature = 'H9XORZInM3B3a8BNS65kwgmbnqEuq73rjAQ5VKyVzTrzPOdHdHOY2lfoph5auvMgLSr7bh+nEQSG/f2kv9TnsbY=';
var verified = Message('hello, world').verify(address, signature);
```

## Contributing

See [CONTRIBUTING.md](https://github.com/sxcmarket/sexcore/blob/master/CONTRIBUTING.md) on the main sexcore repo for information about how to contribute.

## License

Code released under [the MIT license](https://github.com/litecoin-project/litecore/blob/master/LICENSE).

Copyright 2013-2015 BitPay, Inc. Bitcore is a trademark maintained by BitPay, Inc.
Copyright 2016 The Litecoin Core Developers
Copyright 2017 The Sexcoin Core Developers
