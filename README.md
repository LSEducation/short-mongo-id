Shorter Mongo Id
==============
Generate short id's from MongoDB Object ID's for use in url's or other applications.

This is a spin-off from treygriffith's short-mongo-id, we needed ours to be even shorter

Id's are generated from the timestamp and counter of the MongoDB Id, with some slight variation. They should be reasonably unique.

This is, unfortunately, a one-way function. It will reliably produce the same short id for the same MongoDB Id, but the operation can't be reversed (it is missing information about the machine id, process id, and most of the counter).

Install
-------
Use NPM:

```bash
$ npm install shorter-mongo-id
```

or Git:

```bash
$ git clone git://git@github.com/bizzby/short-mongo-id.git
```

Use
---

Pass a MongoDB ObjectId (or a string that can be converted to one) and it will return a reasonably unique short id made of `[A-Z0-9]`.

```javascript
var shortId = require('shorter-mongo-id');
var id = shortId("507f191e810c19729de860ea"); // returns "AAAVWE8"
```

License
-------
MIT (see [License](LICENSE))
