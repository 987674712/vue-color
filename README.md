# vue-color 

Color Pickers for Sketch, Photoshop, Chrome & more with Vue.js(vue2.0).  

## [Live demo](http://xiaokaike.github.io/vue-color/)

![intro](./intro.png)

## Installation

### NPM
```bash
$ npm install vue-color
```

### CommonJS
```js
var Photoshop = require('vue-color/src/Photoshop.vue');

new Vue({
  components: {
    'Photoshop': Photoshop
  }
})
```

### ES6
```js
import { Photoshop } from 'vue-color'

new Vue({
  components: {
    'photoshop-picker': Photoshop
  }
})
```

### Browser globals
The `dist` folder contains `vue-color.js` and `vue-color.min.js` with all components exported in the <code>window.VueColor</code> object. These bundles are also available on NPM packages.

```html
<script src="path/to/vue.js"></script>
<script src="path/to/vue-color.min.js"></script>
<script>
  var Photoshop = VueColor.Photoshop
</script>
```

## Local setup

```
npm install
npm run dev
```

## Usage
```js

var defaultProps = {
  hex: '#194d33',
  hsl: {
    h: 150,
    s: 0.5,
    l: 0.2,
    a: 1
  },
  hsv: {
    h: 150,
    s: 0.66,
    v: 0.30,
    a: 1
  },
  rgba: {
    r: 25,
    g: 77,
    b: 51,
    a: 1
  },
  a: 1
}

new Vue({
  el: '#app',
  components: {
    'material-picker': material,
    'compact-picker': compact,
    'swatches-picker': swatches,
    'slider-picker': slider,
    'sketch-picker': sketch,
    'chrome-picker': chrome,
    'photoshop-picker': photoshop
  },
  data: {
    colors: defaultProps
  }
})

```

```html
<!-- suppose you have the data 'colors' in your component -->
<material-picker v-model="colors" @change-color="onChange"></material-picker>
<compact-picker v-model="colors" @change-color="onChange"></compact-picker>
<swatches-picker v-model="colors" @change-color="onChange"></swatches-picker>
<slider-picker v-model="colors" @change-color="onChange"></slider-picker>
<sketch-picker v-model="colors" @change-color="onChange"></sketch-picker>
<chrome-picker v-model="colors" @change-color="onChange"></chrome-picker>
<photoshop-picker v-model="colors" @change-color="onChange"></photoshop-picker>
```

```javascript
// onChange method called when the event 'change-color' is emitted
onChange (val) {
  this.colors = val
}
```

## TODO
-[] docs
-[] more components


## License

vue-color is licensed under [The MIT License](LICENSE).
