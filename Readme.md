# Migration of mongoose 5.x to 6.x
- update mongoose to 6.x
- useNewUrlParser, useCreateIndex and other options are not needed anymore.
- `.populate()` throws an error if to-be-populated field is not defined in schema. Setting `strictPopulate: false` to resolve the issue.
- `document.populate` method is not chainable, using multiple `.populate` calls in /controllers/campground.js @ line:35.