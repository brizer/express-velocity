# Express-velocity

An simple wrap for velocity template engine when using it in express.

## usage

``` js
var express = require('express');
var vm = require('express-velocity');


var app = express();

app.engine(".vm", vm({
  root: __dirname + "/view"  //duplicated with views setting but required for velocity template
}))
app.set("views", __dirname + "/view")
app.set('view engine', '.vm')
app.render("index.vm", function( err, content ){
  assert(content === '<body>hello</body>')
})

```
