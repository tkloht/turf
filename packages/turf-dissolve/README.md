# @turf/dissolve

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

## dissolve

Dissolves a FeatureCollection of [polygon](polygon) features, filtered by an optional property name:value.
Note that [mulitpolygon](mulitpolygon) features within the collection are not supported

**Parameters**

-   `featureCollection` **[FeatureCollection](https://tools.ietf.org/html/rfc7946#section-3.3)&lt;[Polygon](https://tools.ietf.org/html/rfc7946#section-3.1.6)>** input feature collection to be dissolved
-   `options` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** Optional parameters (optional, default `{}`)
    -   `options.propertyName` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)?** features with equals 'propertyName' in `properties` will be merged

**Examples**

```javascript
var features = turf.featureCollection([
  turf.polygon([[[0, 0], [0, 1], [1, 1], [1, 0], [0, 0]]], {combine: 'yes'}),
  turf.polygon([[[0, -1], [0, 0], [1, 0], [1, -1], [0,-1]]], {combine: 'yes'}),
  turf.polygon([[[1,-1],[1, 0], [2, 0], [2, -1], [1, -1]]], {combine: 'no'}),
]);

var dissolved = turf.dissolve(features, {propertyName: 'combine'});

//addToMap
var addToMap = [features, dissolved]
```

Returns **[FeatureCollection](https://tools.ietf.org/html/rfc7946#section-3.3)&lt;[Polygon](https://tools.ietf.org/html/rfc7946#section-3.1.6)>** a FeatureCollection containing the dissolved polygons

<!-- This file is automatically generated. Please don't edit it directly:
if you find an error, edit the source file (likely index.js), and re-run
./scripts/generate-readmes in the turf project. -->

---

This module is part of the [Turfjs project](http://turfjs.org/), an open source
module collection dedicated to geographic algorithms. It is maintained in the
[Turfjs/turf](https://github.com/Turfjs/turf) repository, where you can create
PRs and issues.

### Installation

Install this module individually:

```sh
$ npm install @turf/dissolve
```

Or install the Turf module that includes it as a function:

```sh
$ npm install @turf/turf
```
