Heroku buildpack: Vert.x
========================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpack) for [Vert.X](http://vertx.io/) apps.

Usage
-----

Example usage:

    $ ls
    app.js

    $ heroku create --stack cedar --buildpack https://github.com/jconsid/heroku-buildpack-vertx-jdk7
	
	$ git push heroku master

    -----> Heroku receiving push
    -----> Fetching custom build pack... done
    -----> Vert.x app detected
    -----> Installing Vert.x..... done

The buildpack will detect your app as a Vert.x project if it has a file called server.js. If you don't provide a Procfile, the build pack will default to launching your app with `vertx run server.js`
