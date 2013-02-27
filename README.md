# jquery-html

A function to get a window and the $ out of an HTML source

## Getting Started
Install the module with: `npm install jquery-html`

```javascript
var jquery = require('jquery-html');

jquery.create(function(window,$,free)
{
   $('body').append('ciao!');
   console.log(jquery.source(window));
   free();
});

```
or try with your html

```javascript
var jquery = require('jquery-html');

jquery.create('<!DOCTYPE html>\n<html><body>ciao!</body></html>',
function(window,$,free)
{
   $('body').append('<div>world</div>');
   console.log(jquery.source(window));
   free();
});

```

## License
Copyright (c) 2013 Andrea Amerigo Aristodemo Gariboldi  
Licensed under the MIT license.
