

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

==
video 22

Darrens-Air:src kub3r$ pwd
/Users/kub3r/Desktop/mean/codesnippets/src
Darrens-Air:src kub3r$
Darrens-Air:src kub3r$
Darrens-Air:src kub3r$ git init
Reinitialized existing Git repository in /Users/kub3r/Desktop/mean/codesnippets/src/.git/
Darrens-Air:src kub3r$
Darrens-Air:src kub3r$ git add .
Darrens-Air:src kub3r$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   DARREN_README.txt
	modified:   bower.json
	deleted:    modules/articles/client/articles.client.module.js
	deleted:    modules/articles/client/config/articles.client.config.js
	deleted:    modules/articles/client/config/articles.client.routes.js
	deleted:    modules/articles/client/controllers/articles.client.controller.js
	deleted:    modules/articles/client/services/articles.client.service.js
	deleted:    modules/articles/client/views/create-article.client.view.html
	deleted:    modules/articles/client/views/edit-article.client.view.html
	deleted:    modules/articles/client/views/list-articles.client.view.html
	deleted:    modules/articles/client/views/view-article.client.view.html
	deleted:    modules/articles/server/config/articles.server.config.js
	deleted:    modules/articles/server/controllers/articles.server.controller.js
	deleted:    modules/articles/server/models/article.server.model.js
	deleted:    modules/articles/server/policies/articles.server.policy.js
	deleted:    modules/articles/server/routes/articles.server.routes.js
	deleted:    modules/articles/tests/client/articles.client.controller.tests.js
	deleted:    modules/articles/tests/e2e/articles.e2e.tests.js
	deleted:    modules/articles/tests/server/article.server.model.tests.js
	deleted:    modules/articles/tests/server/article.server.routes.tests.js
	deleted:    modules/chat/client/chat.client.module.js
	deleted:    modules/chat/client/config/chat.client.config.js
	deleted:    modules/chat/client/config/chat.client.routes.js
	deleted:    modules/chat/client/controllers/chat.client.controller.js
	deleted:    modules/chat/client/css/chat.css
	deleted:    modules/chat/client/views/chat.client.view.html
	deleted:    modules/chat/server/sockets/chat.server.socket.config.js
	deleted:    modules/chat/tests/client/chat.client.controller.tests.js
	deleted:    modules/chat/tests/e2e/chat.e2e.tests.js
	deleted:    modules/chat/tests/server/chat.socket.tests.js
	modified:   package.json

Darrens-Air:src kub3r$
this is different to that shown in the video so I think somehow I already
have a git repository on my laptop that this code is in but I'm not sure how
and when it was created
