<!-- 
<link rel="stylesheet" href="lib/atom-highlight.css">
<link href="https://fonts.googleapis.com/css?family=Fira+Mono|Rubik:300,400" rel="stylesheet">
<script src="lib/highlight.pack.js"></script>
<script>hljs.initHighlightingOnLoad();</script>
-->

Hi! 

---

I'm Molly

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
- ✨ style many different features in the same layer
- ✨ fewer layers 🚀 more efficient rendering 

---

# Property function looks like this 👇

```js
{
  "circle-radius": {
    "stops": [

      // zoom is 5 -> circle radius will be 1px
      [5, 1],

      // zoom is 10 -> circle radius will be 2px
      [10, 2]
    ]
  }
}
```
---

# Zoom-and-property function looks like this 👇

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



---

# Contribute! 

- [mapbox-gl-js starter issues](https://github.com/mapbox/mapbox-gl-js/issues?q=is%3Aopen+is%3Aissue+label%3A%22starter+task%22)
- [mapbox-gl-native issues](https://github.com/mapbox/mapbox-gl-native/issues)

---

# Calaphon

- [biggie](https://github.com/tmcw/biggie)

