# Vue + Express + MongoDB App Boilerplate

I wanted to create some boilerplate to get up and running with a Vue, Express and MongoDB stack.  Specifically with separate API and front-end layers.


## api/

The API layer comprises:

- express
- logging with Morgan
- npm-watch for hot reload
- tape for unit tests

## front-end/

Front-end includes:

- default vue-cli app
- intialised with:
	- linting - airbnb style
	- webpack with hot-reload
	- karma unit testing
	- e2e test with PhantomJS
	- axios for API connectivity
- dev proxyTable reroutes API calls to the connected docker API instance

## Docker
Docker compose handles bringing this stack live with api, front-end and database layers. Volumes used to keep hot-reloading in place for each container without having to rebuild.

## Usage 
`docker-compose up`

Visit front-end on `localhost:8080`, API listens on `localhost:3000`

