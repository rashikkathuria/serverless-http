# serverless-http

## Description

This module allows you to 'wrap' your API for serverless use. No HTTP server, no ports or sockets. Just your code in the same execution pipeline you are already familiar with.

Before using this module, you should already understand API Gateway and AWS Lambda. Specifically, you *must* be using Proxy Integration.

## Usage

You can use `express` (or `connect`) instead of `koa` - it's all the same:

```javascript
const serverless = require('serverless-http');
const koa = require('koa');

// construct your app as normal
const app = koa();
// register your middleware as normal
app.use(/* ... */);

// this is it!
module.exports.handler = serverless(app);
```

## Contributing

Pull requests are welcome! Especially test scenarios for different situations (e.g. multipart, static file serving)