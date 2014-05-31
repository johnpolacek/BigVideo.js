# BigVideo.js
## The jQuery Plugin for Big Background Video (and Images)

Find out everything you need to know about how to use this plugin on its demo page at <http://dfcb.github.com/BigVideo.js>.

## Installation
If you're using [Bower](http://bower.io) (and you should be!) installing BigVideo and its dependencies is simply:

```
bower install BigVideo.js
```

This downloads and installs BigVideo to the ``bower_components`` folder. Add to your page the usual way with script tags, or using [RequireJS](#requirejs).

If you'd rather download things manually, you can grab the latest zip from that lovely button on the right ([or this link](https://github.com/dfcb/BigVideo.js/archive/master.zip)). You will also need the dependencies:

* [jQuery 1.7.2 or higher](http://jquery.com/download)
* [jQuery UI slider 1.8.22 or higher](http://jqueryui.com/download/#!components=1110000000000000100000000000000000)
* [Video.js 3.2 or higher](http://www.videojs.com/)
* [imagesloaded 2.1.1 or higher](http://desandro.github.io/imagesloaded/)

## RequireJS
If [RequireJS](http://requirejs.org/) is detected, BigVideo.js defines itself as an anonymous module. Require it as:

```javascript
require(['path/to/bigvideo'], function(bigvideo) {
	// do stuff here
});
```

Make sure your [require config](http://requirejs.org/docs/api.html#config) is set up correctly; an example configuration is as follows:

```javascript
require.config({
	paths: {
		"BigVideo": "bower_components/BigVideo/lib/bigvideo",
		"jquery": "bower_components/jquery/jquery",
		"jquery-ui": "bower_components/jquery-ui/ui/jquery-ui",
		"videojs": "bower_components/video.js/video",
		"imagesloaded": "bower_components/imagesloaded/imagesloaded",
		"eventEmitter/EventEmitter": "bower_components/eventEmitter/EventEmitter",
		"eventie/eventie": "bower_components/eventie/eventie"
	},
	shim: {
		"videojs": {exports: 'videojs'}
	}
});
```

This is to ensure that BigVideo and all its dependencies get the right paths, and that RequireJS knows how to reference Video.js.

* * *
### Created by John Polacek 
Follow [@johnpolacek](https://twitter.com/johnpolacek) on Twitter

Thanks to [Matt Brennan](https://github.com/quarterto) for Bower integration

* * *
### Draftfcb Chicago
We are the development group at Draftfcb Chicago. If you want to work on big digital ideas for big brands, get in touch with us at [devrecruiting@draftfcb.com](mailto:devrecruiting@draftfcb.com).

* * *
The MIT License (MIT)
Copyright © 2012 John Polacek

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
