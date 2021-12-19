# leaflet-geojson-vt

This is a plugin combining geojson-vt with leafletjs, which is inspired by [geojson-vt-leaflet](https://github.com/handygeospatial/geojson-vt-leaflet). I am the original author of leaflet-geojson-vt. [iamtekson/leaflet-geojson-vt](https://github.com/iamtekson/leaflet-geojson-vt) is a fork of this repo. Welcome to use this plugin.

If you use leaflet 0.7, please switch to the [leaflet0.7.7](https://github.com/brandonxiang/leaflet-geojson-vt/tree/leaflet0.7.7).

## Usage

```javascript
var options = {
    maxZoom: 16,
    tolerance: 3,
    debug: 0,
    style: {
        fillColor: '#1EB300',
        color: '#F2FF00',
        weight: 2
    }
};
var canvasLayer = L.gridLayer.geoJson(json, options).addTo(map);
```

Options are included with [geojson-vt options](https://github.com/mapbox/geojson-vt#options) and [L.geojson style](http://leafletjs.com/reference.html#path-options).

```javascript
var tileIndex = geojsonvt(data, {
    maxZoom: 14,  // max zoom to preserve detail on
    tolerance: 3, // simplification tolerance (higher means simpler)
    extent: 4096, // tile extent (both width and height)
    buffer: 64,   // tile buffer on each side
    debug: 0      // logging level (0 to disable, 1 or 2)

    indexMaxZoom: 4,        // max zoom in the initial tile index
    indexMaxPoints: 100000, // max number of points per tile in the index
    solidChildren: false    // whether to include solid tile children in the index
});
```

## Demo

[DEMO](https://brandonxiang.github.io/leaflet-geojson-vt/test)

## Development

run npm script with `browser-sync`

```shell
npm run dev
```

Browser on `http://localhost:3000/example`

## TODO

- point interactive
- ~~new branch to compatiable with 1.0.0~~
- ~~more geojson style~~
- ~~convert to included class of `L.TileLayer.Canvas`~~
- ~~different canvas layers~~
- ~~style for polygon and polyline~~
- ~~layers change~~
- ~~seperate index.js into index.js and app.js~~
- ~~draw point on canvas~~
- ~~draw marker by image(cancel)~~

## Changelog

[changelog](doc/changelog.md)

## License

[brandonxiang@MIT](LICENSE)
