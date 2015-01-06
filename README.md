Knockout-Ace
============

This project provides Knockout bindings for the Ace editor.

## Installation

Simply include the *knockout-ace.js* file in with your project.  You will need to be using AMD (e.g., RequireJS).

If you use Bower, you can install this package from Bower.

	bower install --save knockout-ace

## Usage

See *index.html* for an example.

	<div class="editor" id="myEditor" data-bind="ace: markup2"></div>

This will create an Ace editor bound to the div element.  The content of the editor will be bound to the *markup2* observable.

You can pass options through to Ace like this:

	<div class="editor" id="myEditor" data-bind="ace: markup1, aceOptions: { mode: 'javascript', theme: 'solarized_light' }"></div>

If the div is not given an explicit ID, an ID will be automatically created for it.

## Additional APIs

The field `ko.aceEditors` provides two functions for your convenience.

* `ko.aceEditors.resizeAll()` calls `editor.resize()` for each editor currently registered with Knockout.
* `ko.aceEditors.get(id)` returns a reference to the Ace editor with the specified ID ("myEditor" in the above example).  This reference exposes the entire Ace API for you to play with, enabling you to change the theme, set options on the fly, and so on.
