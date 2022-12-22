# Demo 20221222
This is a demonstration on make a testing framework watch files in a container. The testing framework used in this demo is [Mocha].

Upon looking in the [dependencies] of [Mocha], it uses [Chokidar package] and requires
[`CHOKIDAR_USEPOLLING`] to watch the files. This problem was also faced in [other packages].

## Instructions

### Pre-requisites
- [Docker]
- [Node.js and npm]

### Steps
1. Open Docker desktop application or at least start it is able to run a container.
2. While waiting for the desktop application, run `npm install` in case you want run the tests
	locally first.
3. When Docker is ready to run a container, run `docker compose up -d`.
4. Check the desktop application to confirm that the container is running and view its output.
5. Try to change the results in [sample test](./t/sample.js).
6. You should see that the test will re-run in the container.

## Origin
Some parts of the repository was based from [`empty_package_json`] branch of [Web Template].

### Author
Coded by Kenneth Trecy Tobias.

[Docker]: https://www.docker.com/
[Node.js and npm]: https://nodejs.org/en/
[Mocha]: https://mochajs.org
[Chokidar package]: https://github.com/paulmillr/chokidar
[`CHOKIDAR_USEPOLLING`]: https://github.com/paulmillr/chokidar#performance
[dependencies]: https://github.com/mochajs/mocha/blob/202e9b8b4d1b6611c96d95d631c49d631d88c827/package.json
[other packages]: https://github.com/facebook/create-react-app/issues/10253
[`empty_package_json`]: https://github.com/KennethTrecy/web_template/tree/empty_package_json
[Web Template]: http://github.com/KennethTrecy/web_template
[MIT]: https://github.com/KennethTrecy/web_template/blob/master/LICENSE
