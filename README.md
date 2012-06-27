coffeepot
=========

Connect/Express middleware to dynamically serve coffee files as js


example
-------

app.coffee

    express = require 'express'
    coffeepot = require 'coffeepot'

    app = express.createServer()

    app.configure ->
      publicDir = __dirname + "/public"
      app.use coffeepot publicDir
      app.use express.static publicDir

    app.listen 3000

public/js/test.coffee

    console.log "HI"

Now if you request `http://localhost:3000/js/test.js` it will resolve.

