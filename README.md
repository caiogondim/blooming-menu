<img src="http://rawgit.com/caiogondim/blooming-menu/master/logo/logo.svg">

# BloomingMenu
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat)](https://github.com/feross/standard)

A configurable and animated radial menu.
BloomingMenu is a port of AwesomeMenu for the web.


## Preview

<img src="http://rawgit.com/caiogondim/blooming-menu/master/gif-preview/center.gif">
<img src="http://rawgit.com/caiogondim/blooming-menu/master/gif-preview/bottom-left.gif">


## Install

You can install through [npm](//npmjs.com) and use [browserify](//browserify.org) to make it run on the browser.
```bash
npm install --save blooming-menu
```

Or just download the minified version
[here](https://raw.githubusercontent.com/caiogondim/blooming-menu/master/build/blooming-menu.min.js).


## Usage

Create a new `BloomingMenu` object:
```js
var menu = new BloomingMenu({
  itensNum: 8
})
```

Render it:
```js
menu.render()
```

And now you can attach event listeners to the itens of the menu, just
like a regular DOM element.
```js
menu.props.elements.itens.forEach(function (item, index) {
  item.addEventListener('click', function () {
    console.log('Item #' + index + 'was clicked')
  })
})
```

## API

### constructor `new BloomingMenu(opts)`

Options object passed on instantiation time, e.g.:
```js
var menu = new BloomingMenu({
  startAngle: 60,
  endAngle: 0
})
```

- `opts.itensNum`
  - Type: `Number`
  - Required: true
- `opts.startAngle`
  - Type: `Number`
  - Default: `90`
- `opts.endAngle`
  - Type: `Number`
  - Default: `0`
- `opts.radius`
  - Type: `Number`
  - Default: `80`
- `opts.itemAnimationDelay`
  - Type: `Number`
  - Default: `0.04`
- `opts.animationDuration`
  - Type: `Number`
  - Default: `0.4`
- `opts.fatherElement`
  - Type: `HTMLElement`
  - Default: `document.body`
- `opts.itemWidth`
  - Type: `Number`
  - Default: 50
- `opts.CSSClassPrefix`
  - Type: `String`
  - Default: `'blooming-menu__'`
- `opts.mainContent`
  - Type: `String`
  - Default: `'+'`
- `opts.injectBaseCSS`
  - Type: `Boolean`
  - Default: `true`


Every method below is an instance method.

### obj.`render`

Attachs the instance to the DOM and binds all event listeners.

### obj.`remove`

Removes all DOM elements and event listeners.

### obj.`open`

Opens the menu programmatically.

### obj.`close`

Closes the menu programmatically.

### obj.`selectItem(num)`

Select programatically the `num` item of the menu.


## Credits
- Project icon by Chamaquito Pan de Dulce
- Menu items by [Google Material Design](https://github.com/google/material-design-icons)
- [Base16](https://github.com/chriskempson/base16) Ocean color scheme
- This lib is a port in JavaScript of the Objective-C lib [AwesomeMenu](https://github.com/levey/AwesomeMenu)
