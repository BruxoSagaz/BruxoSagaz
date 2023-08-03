const { addonBuilder, serveHTTP } = require('stremio-addon-sdk');

const manifest = {
  id: 'com.example.catalog',
  version: '1.0.0',
  name: 'Example Catalog Addon',
  description: 'A simple catalog addon for Stremio',
  catalogs: [],
  resources: ['catalog'],
  types: ['movie'],
};

const builder = new addonBuilder(manifest);

builder.defineCatalogHandler(args => {
  return Promise.resolve({ metas: [] }); // You can populate this array with actual movie data
});

const addonInterface = builder.getInterface();
serveHTTP(addonInterface, { port: 7000 });
