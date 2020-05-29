# Vue Rough Notation

![npm](https://img.shields.io/npm/v/vue-rough-notation)
![npm bundle size](https://img.shields.io/bundlephobia/minzip/vue-rough-notation)
![GitHub](https://img.shields.io/github/license/Leecason/vue-rough-notation)

![Rough Notation logo](https://roughnotation.com/images/social.png)

A Vue wrapper for [RoughNotation](https://roughnotation.com/), a small JavaScript library to create and animate annotations on a web page.

[Visit website to see it in action](https://roughnotation.com/)

## Installation

NPM:

```shell
npm install --save vue-rough-notation
```

CDN:

```js
<script src="https://unpkg.com/vue-rough-notation/dist/vue-rough-notation.js"></script>
```

## Usage

main.js:

```js
import VueRoughNotation from 'vue-rough-notation';

Vue.use(VueRoughNotation);
```

template:

```html
<RoughNotation
  :is-show="isShow"
  type="underline"
>
  <span>Rough Notation is awesome</span>
</RoughNotation>
```

## Props

### type

**Type**: `string`

**required**: `true`

This is a mandatory field. It sets the annotation style. Following are the list of supported annotation types:

- **underline**: Create a sketchy underline below an element.
- **box**: This style draws a box around the element.
- **circle**: Draw a circle around the element.
- **highlight**: Creates a highlight effect as if maked by a highlighter.
- **strike-through**: This style draws a box around the element.
- **crossed-off**: This style draws a box around the element.

### isShow

**Type**: `boolean`

**Required**: `false`

**Default**: `false`

Whether draws the annotation.

### animate

**Type**: `boolean`

**Required**: `false`

**Default**: `true`

Turn on/off animation when annotating.

### animationDuration

**Type**: `number`

**Required**: `false`

**Default**: `800`

Duration of the animation in milliseconds.

### animationDelay

**Type**: `number`

**Required**: `false`

**Default**: `0`

Delay in animation in milliseconds.

### color

**Type**: `string`

**Required**: `false`

**Default**: `currentColor`

Representing the color of the annotation sketch.

### strokeWidth

**Type**: `number`

**Required**: `false`

**Default**: `1`

Width of the annotation strokes.

### padding

**Type**: `number`

**Required**: `false`

**Default**: `5`(in pixels)

Padding between the element and roughly where the annotation is drawn.

### tag

**Type**: `string`

**Required**: `false`

**Default**: `'div'`

String HTML tag name (default: `div`); if falsy (for example `null` or `undefined`), the component will be renderless (the content won't be wrapped in a tag), in this case, only the first child will be rendered

## Events

### init

**Parameters**: [`Annotation Object`](https://github.com/pshihn/rough-notation#annotation-object)

Called when the component is initialized.

## TODO

- [ ] Annotation Group
- [ ] Demo pages

## License

[MIT](https://github.com/Leecason/vue-rough-notation/blob/master/LICENSE)
