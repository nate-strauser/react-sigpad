[![npm package](https://img.shields.io/npm/v/react-sigpad?style=plastic)](https://www.npmjs.com/package/react-sigpad)

# React Signature Pad
A [signature pad](https://github.com/szimek/signature_pad) implementation for react.

#### _Forked at version 0.0.9 after package removed from npm
#### _Forked at version 0.0.6 to force signature redraw on canvas resize_

# Basic Usage

```javascript
var React = require('react');
var SignaturePad = require('react-signature-pad');

React.render(
  <SignaturePad clearButton="true" />,
  document.body
)
```

# Methods

```javascript
<SignaturePad clearButton="true" ref="mySignature" />
...

var signature = this.refs.mySignature;

// Methods

// ===============================================
// isEmpty() - returns boolean
// ===============================================

signature.isEmpty();

// ===============================================
// clear() - clears canvas
// ===============================================

signature.clear();

// ===============================================
// toDataURL() - retrieves image as a data url
// ===============================================

signature.toDataURL();

// ===============================================
// fromDataURL() - writes a base64 image to canvas
// ===============================================

signature.fromDataURL(base64String);

```

# CSS
In order to make the signature pad work correctly you will need the css as well.  All the relevant styles are in [this file](style.css).

# Example
```bash
$ npm start
```
Then navigate to http://localhost:8080/ in your browser and you should be able to see the signature pad in action.

# Change Log

- v0.0.9
- (2017-05-25) add support for `className` prop to allow attaching optional classnames for styling purposes
- (2017-01-09) fix issue where `isEmpty` is `false` on initial component mount with no data
- (2016-12-05) force signature redraw on canvas resize event