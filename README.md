
pa11y-web
=========

pa11y-web is a visual web interface to the [pa11y][pa11y] accessibility reporter.

**Current Version:** *0.0.0*  
**Node Version Support:** *0.10*


Setup
-----

pa11y-web requires [Node.js][node] 0.10+ and [pa11y-webservice][pa11y-webservice] to be installed and running. You'll need to follow the setup guide for pa11y-webservice before setting up pa11y-web.

You'll then need to clone this repo locally and install dependencies with `npm install`. Once you have a local clone, you'll need to copy some sample configuration files in order to run the application. From within the repo, run the following commands:

```sh
$ cp config/development.sample.json config/development.json
$ cp config/production.sample.json config/production.json
```

Each of these files defines configurations for a different environment. If you're just running the application locally, then you should be OK with just development configurations. The [available configurations are documented here](#configurations).

Now that you've got your application configured, you can run in each mode with the following commands:

```sh
$ make start       # start in production mode
$ make start-dev   # start in development mode
```

Development mode runs the application with [Supervisor][supervisor], so you won't need to restart it if you change any JavaScript files.


Configurations
--------------

The boot configurations for pa11y-web are as follows. Look at the sample JSON files in the repo for example usage.

### webservice
*(string)* The base URL of the [pa11y-webservice][pa11y-webservice] instance you intend on using.

### port
*(number)* The port to run the application on.


License
-------

[Copyright 2013 Nature Publishing Group](LICENSE.txt).  
pa11y-web is licensed under the [GNU General Public License 3.0][gpl].



[gpl]: http://www.gnu.org/licenses/gpl-3.0.html
[node]: http://nodejs.org/
[pa11y]: https://github.com/nature/pa11y
[pa11y-webservice]: https://github.com/nature/pa11y-webservice
[supervisor]: https://github.com/isaacs/node-supervisor