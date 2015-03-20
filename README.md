Heroku or Dokku buildpack: Node.js with bower + grunt support
============================================

add a env var to your app

dokku config:set $APP BUILDPACK_URL=https://github.com/sibeliusseraphini/heroku-buildpack-nodejs-bower-grunt

or in your repository .env
export BUILDPACK_URL=https://github.com/sibeliusseraphini/heroku-buildpack-nodejs-bower-grunt

set a NODE_ENV var:

dokku config:set $APP NODE_ENV=prod

A high level description of the script:
- install npm
- install bower
- install grunt
- restore node_modules cache
- restore bower_components cache
- npm install
- bower install
- cache node_modules
- cache bower_components
- grunt build:$NODE_ENV

Thanks for the forked repository and the heroku buildpack node.js



























































































