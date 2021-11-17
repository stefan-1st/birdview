# Birdview.js

![Screenshot](birdview_banner.png)

**Get a glance at a whole web page with an aerial view.**

See [**demo & full documentation here**](https://www.achrafkassioui.com/birdview/).

## Setup

Include `birdview.js` and `birdview.css` in HTML:

```
<link rel="stylesheet" type="text/css" href="birdview.css"/>
<script type="text/javascript" src="birdview.js"></script>
```

Then enable Birdview with the initialization method:

```
birdview.init();
```

## Usage

To trigger birdview, you can either:

- **Press the Z key**
- **Pinch-in** on a touch device

You can also trigger birdview by clicking any HTML element with a `birdview_toggle` class:

```html
<button class="birdview_toggle">Birdview</button>
```

Or you can toggle birdview programmatically using the toggle method:

```javascript
birdview.toggle();
```

There are a few options available so you can tweak birdview the way you need it.

```javascript
	const defaults = {
		shortcut: 90,
		button: true,
		button_text: 'Birdview',
		speed: 0.3,
		easing: 'ease',
		overlay: true,
		overlay_transition: 0.3,
		origin_X: 50,
		callback_start: null,
		callback_end: null,
		touch: true,
		debug: false,
		text_h1: 'Birdview',
		text_close: 'X',
		text_home: 'Home',
		text_title: document.title,
		text_usage: 'Click to dive<br>Press Z or pinch to toggle birdview',
		text_zooming: 'Zooming...'
	};
```

Let's say you want to change the zooming text to something different:

```javascript
birdview.toggle({
    text_zooming: 'Watch the magic happen...'
});
```



You can stop birdview from running on your page by calling:

```javascript
birdview.destroy();
```

The destruction method is called inside the initialization method. Calling `birdview.init()` multiple times shouldn't create any undesirable overlapping.

## License

Birdview.js is published under the [GNU General Public License](https://www.gnu.org/licenses/gpl-3.0.en.html).
