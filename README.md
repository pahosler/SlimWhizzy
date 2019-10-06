# SlimWhizzy
SlimWhizzy is a light weight and depedency free library for adding WYSIWYG functionality to an contenteditable element. You simply create your editor
to your liking, and then add a single function call with a few configuration items and you are in business.

[Demo](https://slimwhizzy.jodylecompte.com/)

## Install

SlimWhizzy can be installed via NPM
```
npm install slimwhizzy --save
```
Or you can simply download / clone this repo and make use of the minified production copy ```SlimWhizzy.min.js```

## Usage
Slim Whizzy is intended to be used as a front end asset and included as such, and is released on NPM for convinience / consistency with other workflows. Once you include the Javascript file in your source, there are just a few things that need to be done to make your editor compatible with SlimWhizzy.

### Example of Initialization
```
SlimWhizzy({
  btnClass: '.toolbar-button',
  editorSelector: '.editor'
});
```

### Configuration Options
* **btnClass** - The class that each button will have that allows SlimWhizzy to attach the event handler
* **editorSelector** - The selector (can be an ID or class) for the contenteditable element serving as the editor

```btnClass``` and ```editorSelector``` are optional and will default to the settings shown in the example above if left blank

### Assigning Commands
The following commands are supported. They can be implemented by adding ```data-command="<item>"``` where ```<item>``` is the desired value supplied in parenthesis below. 

* Headers (h1, h2, h3, h4, h5, h6)
* Paragraphs (p)
* Links (createlink, unlink)
* Image (insertimage)
* Text Formatting (bold, italic, underline, strikethrough, subscript, superscript)
* Text Justification (justifyLeft, justifyCenter, justifyRight, indent, outdent)
* Lists (insertOrderedList)
* Ooops! (redo, undo)

### Saving / Loading
Saving and loading are still in development and will be accomplished by callbacks provided to the SlimWhizzy constructor, alternatively you can simply attach your own save / load logic to the 
editor and not attach the button class supplied to the configuration so that SlimWhizzy will ignore your save button. 

## Contributing
Contributions are welcome and greatly appreciated. There is no formal policy in place currently other than opening an issue for discussion or commenting on an existing issue before submitting 
a PR. 

