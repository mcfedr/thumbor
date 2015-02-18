# ThumborUrlBuilder

Thumbor client for Node JS

Combination of
- https://github.com/dcaramelo/ThumborUrlBuilder crypt implementation
- https://github.com/rafaelcaricio/ThumborJS build command set

Neither of these repos are updating anymore so we are maintaining our own

## Usage

```sh
# Install thumbor module

npm install thumbor
```

```javascript
// Declare thumbor-url-builder in JS
// Your encryption key is not required, but your link will be unsafe.

var Thumbor = require('thumbor');
var thumbor  = new Thumbor('MY_KEY', 'http://myserver.thumbor.com');

// Generate your url :

var thumborUrl = thumbor.setImagePath('00223lsvrnzeaf42.png').resize(50,50).buildUrl();
```


# Bower Usage

This module can be installed

    bower install thumbor
    
If you use a secret key, you must include the dependency.

    <script src="bower_components/jssha/src/sha1.js"></script>
    <script src="bower_components/thumbor/index.js"></script>
    
You can set the key to be null and it will generate unsafe urls. This might be preferable as putting your key into most
javascript isn't very secure!
