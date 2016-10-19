<!-- 
<link rel="stylesheet" href="lib/atom-highlight.css">
<link href="https://fonts.googleapis.com/css?family=Fira+Mono|Rubik:300,400" rel="stylesheet">
<script src="lib/highlight.pack.js"></script>
<script>hljs.initHighlightingOnLoad();</script>
-->

Hi! 

---

- 🐧 @mollymerp
- 👾 [github.com/mollymerp](https://www.github.com/mollymerp)
- 📝 molly@mapbox.com

---

# Mapbox GL

- ⚡️ vector tiles + style.json + 💻 | 📱= 🗺
- ⚡️ fast, customizable, cross-platform
- ⚡️ run-time styling

---

# Data driven styling _aka_ property functions _aka_ zoom-and-property functions

- ✨ use data in your vector tiles or GeoJSON
- ✨ style many different feature types in the same layer
- ✨ fewer layers 🚀 more efficient rendering 

---

# A property function looks like this 👇

```js
{
  "circle-color": {
    "property": "temperature",
    "stops": [

      // "temperature" is 0   -> circle color will be blue
      [0, 'blue'],

      // "temperature" is 100 -> circle color will be red
      [100, 'red']

    ]
  }
}
```
---

# A zoom-and-property function looks like this 👇

```js
{
  "circle-radius": {
    "property": "rating",
    "stops": [

      // zoom is 0 and "rating" is 0 -> circle radius will be 0px
      [{zoom: 0, value: 0}, 0],

      // zoom is 0 and "rating" is 5 -> circle radius will be 5px
      [{zoom: 0, value: 5}, 5],

      // zoom is 20 and "rating" is 0 -> circle radius will be 0px
      [{zoom: 20, value: 0}, 0],

      // zoom is 20 and "rating" is 5 -> circle radius will be 20px
      [{zoom: 20, value: 5}, 20]

    ]
  }
}
```
---
# Map design

- ● [Mapbox Streets](https://www.mapbox.com/maps/streets/)

  - ⚬ 186 layers
  - ⚬ 80 "road" + "bridges" layers w/ same source

- ● With `line` property functions, layer count 📉

---
# Extrusions _aka_ 3D 🌆 and more! 

- ● Data driven styling allows buildings to be rendered realistically
- ● Mapbox Streets includes `height` and `min-height` properties

---

Data visualization 🎨📊👓

- 🚀 we're adding more supported properties with every release
- 💁 [mapbox-gl-style-spec](https://www.mapbox.com/mapbox-gl-style-spec/#layers-fill)

---

# Contribute! 

- All of this is open source. 
- [mapbox-gl-js starter issues](https://github.com/mapbox/mapbox-gl-js/issues?q=is%3Aopen+is%3Aissue+label%3A%22starter+task%22)
- [mapbox-gl-native issues starter issues](https://github.com/mapbox/mapbox-gl-native/issues?q=is%3Aopen+is%3Aissue+label%3Astarter-task)

---

# Thanks! 
