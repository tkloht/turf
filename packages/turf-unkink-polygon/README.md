# @turf/unkink-polygon

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

## unkinkPolygon

Takes a kinked polygon and returns a feature collection of polygons that have no kinks.
Uses [simplepolygon](https://github.com/mclaeysb/simplepolygon) internally.

**Parameters**

-   `geojson` **([FeatureCollection](https://tools.ietf.org/html/rfc7946#section-3.3) \| [Feature](https://tools.ietf.org/html/rfc7946#section-3.2)&lt;([Polygon](https://tools.ietf.org/html/rfc7946#section-3.1.6) \| [MultiPolygon](https://tools.ietf.org/html/rfc7946#section-3.1.7))>)** GeoJSON Polygon or MultiPolygon

**Examples**

```javascript
var poly = turf.polygon([[[0, 0], [2, 0], [0, 2], [2, 2], [0, 0]]]);

var result = turf.unkinkPolygon(poly);

//addToMap
var addToMap = [poly, result]
```

Returns **[FeatureCollection](https://tools.ietf.org/html/rfc7946#section-3.3)&lt;[Polygon](https://tools.ietf.org/html/rfc7946#section-3.1.6)>** Unkinked polygons

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
$ npm install @turf/unkink-polygon
```

Or install the Turf module that includes it as a function:

```sh
$ npm install @turf/turf
```
