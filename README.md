# webkit-touch-scroll-fix

> Fixes the [iOS 11.3 bug](https://bugs.webkit.org/show_bug.cgi?id=184250) that makes touch events cause the window to scroll.  This can be an issue for drag and drop libraries.

This fix was taken directly from a pull request in [react-beautiful-dnd](https://github.com/atlassian/react-beautiful-dnd/pull/416/files). I thought it might be useful for it to be its own package.

## Usage

```js
const webkitHack = require('webkit-touch-scroll-fix')

const onDrag = (e) => {
  webkitHack.preventTouchMove()
}
const onDragStop = (e) => {
  webkitHack.releaseTouchMove()
}
```

## Install

With [npm](https://npmjs.org/) installed, run

```
$ npm install webkit-touch-scroll-fix
```

## License

MIT

