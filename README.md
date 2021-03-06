# simplespinner jQuery plugin
A simple spinner with a customizable label.


## Setup
Include both `simple-spinner.js` and `simple-spinner.css` files to your html page  

```html
<link rel="stylesheet" href="simple-spinner.css" />
<script src="simple-spinner.js"></script>
```

## Usage
You simply need to call the `simplespinner()` on container element (usually `body`) for that spinner, keep its reference and later show or hide it when necessary

```javascript
var spinner = $('body').simplespinner();
spinner.show()// shows the spinner
spinner.hide()// hides the spinner
```

It allows you to have multiple spinners for different sections of your page

### Example
```javascript
$(function(){
	var spinner = $('body').simplespinner();

	spinner.show()// shows the spinner

	setTimeout(function(){
		spinner.hide()// hides the spinner
	}, 3000)
})
```

## Options
You can provide few options to `simplespinner(options)` function call.

```javascript
$('body').simplespinner({
	label: 'Please wait...'	
})
```

There are few more options available, but those are all related to modify css clases for spinner elements. **We don't recommend changing those other options unless you're trying to customize styles for your spinner and not happy with our classes names.**


```javascript
$('body').simplespinner({
	label: 'Please wait...',
	spinnerClass: 'simplespinner',
	iconClass: 'simplespinner__figure',
	labelClass: 'simplespinner__label',
	containerLoadingClass: 'simplespinner_loading'
})
```

Here is the list of all options available

Option | Default | Purpose
---|---|---
label|Loading...| Label under the spinner icon
spinnerClass|`simplespinner`| `div` wrapping the spinner icon and label
iconClass|`simplespinner__figure`| Spinner icon
labelClass|`simplespinner__label`| `class` for label
containerLoadingClass|`simplespinner_loading`| `class` added to container (e.g. `body`) while spinner is visible


## Feedback
Your feedback will be highly appreciated.