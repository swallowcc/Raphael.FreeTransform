Raphael.FreeTransform
====================

  Free transform tool for [Raphaël](http://raphaeljs.com/) elements with many options. Supports dragging, scaling and rotating.

  ![Screenshot](https://github.com/ElbertF/Raphael.FreeTransform/raw/master/screenshot.png)


Example
-------

```html
<script type="text/javascript" src="raphael-min.js"></script>
<script type="text/javascript" src="raphael.free_transform.js"></script>

<div id="foo"></div>

<script type="text/javascript">
	var paper = Raphael(0, 0, 500, 500);

	var rect = paper
		.rect(200, 200, 100, 100)
		.attr('fill', '#f00')
		;

	// Add free transform handle
	paper.freeTransform(rect);

	// Remove free transform handle
	// paper.freeTransform(rect).unplug();
</script>
```

Options
-------

`boundary: { x: int, y: int, width: int, height: int }`

Limits the drag area of the handle (default: dimensions of the paper).

`color: hex`

Sets the color of the handle (default: `#f00`).

`drag: true|false`

Enables/disables dragging (default: `true`).

`rotate: true|false`

Enables/disables rotating (default: `true`).

`scale: int`

Enables/disables scaling (default: `true`).

`size: int`

Sets the size of the handle (n times height, default: `.6`).


Functions
---------

`unplug()`

Removes handle and deletes all values set by the plugin.

`updateHandle()`

Updates handle to reflect the element's properties.
