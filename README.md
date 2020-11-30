# vue-sequential-entrance

> This is initially a fork of https://github.com/deivthings/vue-sequential-entrance to submit a PR, but the author never replied. This version has been rewritten for Vue-3

Vuejs Plugin for creating epic sequential animation entrances with a list of elements.
Zero effort.
Really lightweight

![](demo.gif)

## Installation
In order to use into your vue project
```
npm install vue3-sequential-entrance
```

## How to use ( Global Usage )
Add to your main.js file

```javascript
import sequentialEntrance from 'vue3-sequential-entrance'
import 'vue3-sequential-entrance/vue-sequential-entrance.css'

app.use(sequentialEntrance)
```

And now, in your component file, wrap a list of elements with `<sequential-entrance>` tag
```html
<template>
  <sequential-entrance>
    <div class="box" v-for="app in apps" :key="app">{{ app }}</div>
  </sequential-entrance>
</template>
```

Sequential Entrance comes with four 'flavors': animation entrance from Top, from right, from left and from bottom. By default, it uses from right, but you can select what you want this way:
```html
<sequential-entrance fromTop> [...] </sequential-entrance>

<sequential-entrance fromRight> [...] </sequential-entrance>

<sequential-entrance fromBottom> [...] </sequential-entrance>

<sequential-entrance fromLeft> [...] </sequential-entrance>
```


## Customize with the following Props

### delay
By default, the sequence animation have an interval of 250 milliseconds. If you need a faster or slower entrance animation, you can specify the time in milliseconds.
```html
<sequential-entrance delay="1000"> [...] </sequential-entrance>
```

### animation
If you prefer don't use the built in animations (fromTop,fromRight,fromLeft,fromBottom) and use your custom css animation, you can easily using 'animation' props. Simply, put the class name of your animation and that's it.
```html
<sequential-entrance animation="myCustomAnimationClassName"> [...] </sequential-entrance>
```

You can use css animation libraries like animate.css ( https://daneden.github.io/animate.css/ ). Import the entire css library or only the ones that you are going to use and type the class name in animation prop.

```html
<sequential-entrance animation="bounceIn"> [...] </sequential-entrance>
```

### tag
By default, sequential-entrance render a `<div>` tag wrapping its children, but you can customize the wrapper tag through 'tag' prop
```html
<sequential-entrance tag="section"> [...] </sequential-entrance>
```
