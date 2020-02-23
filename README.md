# Deprecated

Following [request's](https://github.com/request/request) deprecation, Requemise is now also deprecated.

We recommend [note-fetch](https://github.com/node-fetch/node-fetch) as an alternative to Request+Requemise.

# Requemise
Requemise - Promise wrapper for the Request package

## Install
`npm install requemise --save`

## Notes
This package will automatically install Request

## How to use
```javascript
// in your js file
const Requemise = require('requemise');

const options = {
  url: 'myawesomewebsite.com/route',
  method: 'POST',
  headers: {
    'x-api-key': 'qwertyuiop'
  },
  body: {
    data: 'your data'
  },
  json: true
}
// options will be directly passed to the request library, please see https://github.com/request/request#requestoptions-callback all the available options

Requemise.req(options)
.then((response) => {
  // Do something with the response
})
.catch((rejection) => {
  // Do something with reject's value, rejection.error and rejection.response
});
```
