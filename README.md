# redshift-sql 

A very light [node-postgres](https://github.com/brianc/node-postgres) wrapper for running AWS Redshift queries.

## Installation

Download node at [nodejs.org](http://nodejs.org) and install it, if you haven't already.

```sh
npm install redshift-sql --save
```

## Usage

```js
var config = {
  host: 'rs-cluster.us-east-1.redshift.amazonaws.com',
  db: 'dev',
  user: 'rsadmin',
  password: 'rsPassword'
};
var rssql = require('redshift-sql')(config);
var query = 'select * from myTable limit 10';

rssql(query, function cb(err, result) {
  if (err) {
    return console.error(err);
  }
  // do stuff
});

```

## Tests

```sh
npm install
npm test
```

## Dependencies

None

## Dev Dependencies

- [package-json-to-readme](https://github.com/zeke/package-json-to-readme): Generate a README.md from package.json contents


## License

ISC

_Generated by [package-json-to-readme](https://github.com/zeke/package-json-to-readme)_
