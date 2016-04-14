# Layer toggle for Mapbox GL JS

## Install

`npm install mapbox-gl-layers`

(Note the peer dependency on `mapbox-gl`!)

## Use

### CommonJS

```js
var Layers = require('mapbox-gl-layers')

new Layers({
  layers: {
    'ALL PARKS': ['national_park', 'parks'],
    'National Parks': 'national_park',
    'Other Parks': 'parks'
  }
}).addTo(map) // map is the mapbox gl map instance
```

### Standalone script

Add to `<head>`:

```html
<script src='dist/mapbox-gl-layers.js'></script>
<link href='dist/mapbox-gl-layers.css' rel='stylesheet' />
```

And then:
```html
<script>
map.on('style.load', function () {
  new MapboxGLLayers({
    layers: {
      'ALL PARKS': ['national_park', 'parks'],
      'National Parks': 'national_park',
      'Other Parks': 'parks'
    }
  }).addTo(map) // map is the mapbox gl map instance
})
</script>
```


