# Migration of mongoose 5.x to 6.x
- update mongoose to 6.x
  - `npm uninstall mongoose ; npm i mongoose@latest`   
- [useNewUrlParser, useCreateIndex and other options are not needed anymore](https://github.com/sidmirza4/YelpCamp-v2/blob/mongoose-fix/app.js#L27).
- `.populate()` throws an error if to-be-populated field is not defined in schema. Setting `strictPopulate: false` to resolve the issue. See example, [here](https://github.com/sidmirza4/YelpCamp-v2/blob/mongoose-fix/controllers/campgrounds.js#L11)
- `document.populate` method is not chainable, using multiple `.populate` calls in [/controllers/campgrounds.js @ line:35](https://github.com/sidmirza4/YelpCamp-v2/blob/mongoose-fix/controllers/campgrounds.js#L35).
