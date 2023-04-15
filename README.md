<p align="center"><img src="https://github.com/Axorax/fullscr.js/blob/main/fullscr.js.png?raw=true"></img></p>

<p align="center">Go fullscreen on any browser with <strong>one line of code</strong></p>

<br>

Raw size (fullscr.js) => 1.41 kB

Zipped size (fullscr.js) => 0.6 kB

---

## ⚙️ Installation

```js
npm i fullscr
```

**↪ CDN Links:**

* https://cdn.jsdelivr.net/npm/fullscr@1.0.2/fullscr.js

* https://www.unpkg.com/fullscr@1.0.2/fullscr.js

## 📖 Documentation

#### • Go fullscreen with one line of code

```js
fullscr.enableOnEvent('button', 'click');
```

`fullscr.enableOnEvent()` can take in 4 arguments. They are:

```js
fullscr.enableOnEvent('button', 'click', 'div', () => {
    console.log('Fullscreen is not supported!');
});
```

In the above example,

* `'button'` represents element event will get added to
* `'click'` represents the event
* `'div'` represents element that will get fullscreened
* `() => {...}` represents code that will run if fullscreen is not supported

#### • Enable fullscreen

```js
fullscr.enable();
```

#### • Run code if fullscreen is not supported when using `fullscr.enable()`

```js
fullscr.enable(null, () => {
    console.log('Fullscreen is not supported!')
});
```

`null` means that it will make the entire website fullscreen.

#### • Enable fullscreen on an element

```js
fullscr.enable('div');
```

#### • Disable fullscreen

```js
fullscr.disable();
```

You don't need to provide an element to disable fullscreen on as fullscreen can't be enabled for multiple elements.

#### • Run code if fullscreen is not supported when using `fullscr.disable()`

```js
fullscr.disable(() => {
    console.log('Fullscreen is not supported!')
});
```

#### • Toggle fullscreen

```js
fullscr.toggle();
```

This will enable fullscreen if fullscreen is not enabled and disable fullscreen if it is enabled.

Like `fullscr.enable()` you can toggle fullscreen for any element.

```js
fullscr.toggle('div');
```

#### • Check if fullscreen is enabled

```js
console.log(fullscr.isEnabled);
```

Will return true if there is an element which is fullscreen otherwise false

#### • Check if fullscreen is allowed

```js
console.log(fullscr.isAllowed);
```

#### • Get current element which is in fullscreen

```js
console.log(fullscr.element);
```

#### • Add events to fullscreen

```js
fullscr.on('change', () => {
    console.log('Fullscreen changed!');
});
```

Available events for fullscreen are:

* change
* error

#### • Remove events from fullscreen

```js
fullscr.off('change', myEvent);
```

#### • Listen for changes

```js
fullscr.onchange(() => {
    console.log('Fullscreen changed!');
});
```

#### • Listen for errors

```js
fullscr.onerror(() => {
    console.log('An error occured!');
});
```

#### • HTML example

```html
<body>
    <button>Fullscreen</button>

    <script type="module">
        import fullscr from 'https://cdn.jsdelivr.net/npm/fullscr@1.0.2/fullscr.js';

        fullscr.enableOnEvent('button', 'click');
    </script>
</body>
```

---

[Support me on Patreon](https://www.patreon.com/axorax) - 
[Check out my socials](https://github.com/axorax/socials)