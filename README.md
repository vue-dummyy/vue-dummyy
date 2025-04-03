### vue-dummy
## Placeholder Images and Dummy Text for Vue.js

`vue-dummy` is a wrapper around the https://dummyjs.com/ library to expose placeholder Images and Dummy, Lorum Ipsum Text as a vue directive

## Usage

Add to your HTML page:

```html
<script src="https://unpkg.com/vue"></script>
<script src="https://unpkg.com/vue-dummy"></script>
```

or, import into your module `npm install vue-dummy --save-dev`

```js
import Vue from "vue"
import VueDummy from "vue-dummy"

Vue.use(VueDummy)
```

## Dummy Text

```html
<p v-dummy></p>
```

Choose the number of words:
```html
<p v-dummy="150"></p>
```

Choose random amount of words between 3 & 10:
```html
<p v-dummy="'3,10'"></p> <!-- Note: the quotes to pass the expression as a string -->
<p v-dummy:3,10></p> <!-- or, as a Vue argument-->
```

As a component:
```html
<dummy></dummy>
<dummy text="30"></dummy>
<dummy t="1,3"></dummy>
```

## Dummy Images

```html
<img v-dummy="300" />
```

```html
<img v-dummy="'400x300'" /> <!-- Note: the quotes to pass the expression as a string -->
<img v-dummy:400x300 /><!-- or, as a Vue argument -->
<img v-dummy.400x300 /><!-- or, as a Vue modifier -->
```

Use width & height attribues _or, size with CSS_
```html
<img v-dummy width="150" height="150" />
```

Defaults to the size of the parent container
```html
<img v-dummy />
```

Create random sized images. _Useful for testing dimentions of unknown sized user uploaded images_
```html
<img v-dummy="'100,400x200,400'" /> <!-- Note: the quotes to pass the expression as a string -->
<img v-dummy:100,400x200,400 /> <!-- or, as a Vue argument (or modifier) -->
```

As a component:
```html
<dummy img></dummy>
<dummy img="400x300"></dummy>
<dummy i="100"></dummy>
```

## Special Elements

Using `v-dummy` on some tags will result in some placeholder content with expected markup. This is useful in some cases like quick styling of elements
```html
<ol v-dummy></ol> <!-- outputs a small list -->
<ul v-dummy></ul> <!-- outputs a small list -->
<table v-dummy></table> <!-- outputs a small table -->
```

## Example Repeat Elements

Combine with `v-for` to repeat elements

```html
  <ul>
    <li v-for="i in 6" v-dummy>#{{i}}: </li>
  </ul>
```

#### Examples
https://git.io/vue-dummy-example
