

in src:

server.js is where the server is run from. Out of the box it is:

'use strict';

/**
 * Module dependencies.
 */
var app = require('./config/lib/app');
var server = app.start();




package.json - lists the dependencies etc. The modules are
stored in src/node_modules (I screwed up and added an extra dir)

When we do an npm install this is where the modules will be pulled into.

src/config - for server-side code.

src/app - udemy video he has it but the structure must have changed
as I don't have it.

src/public - for front-end files

in /public there is /dist and /lib (udemy also has /modules but I don't)

Udemy has two files in /src/public that I don't have here:
   applications.js - code that glues the Angular modules to the html page
   config.js -
but I do have:
   "humans.txt" (have to use quotes as Atom won't accept txt unquoted)
   "robots.txt"

/public/dist - used by grunt to deploy the "minified" files (xxx.min I think)
   application.js
   application.min.css
   application.min.js

/public/modules - contains the front-end code (but I don't have this folder -
must have been moved somewhere else)

/public/lib - contains front-end dependencies (Angular, JQuery, Bootstrap, etc)

Udemy has:
   src/modules/core -
   src/modules/users - takes care of authentication and authorization
WHERE ARE MINE?? - it seems they now broke it into /users:
   /client
   /server
   /tests

Angular follows mv* model - either MVC or MVMM (model-view-viewmodel)

==BREAK==
video 20 at 4:20
Backend - in Udemy it's in src/app - not sure where it is now, and src/config

config - defines the different environments under which we can run node.

Lecture 21 - Express
The main task of express is to handle the requests coming in to the web server
and then route them to the appropriate handler. "essentially a series of
middleware calls"

src/modules/core/server/routes is now what is used to be in src/app/routes
(video 21 at 2:58)

express.js - is in src/config/lib
