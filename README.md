# BigVideo.js
####The jQuery Plugin for Big Background Video (and Images)
Learn how to use this plugin on its demo page at <http://dfcb.github.com/BigVideo.js>.

##12-30-2015 Update
This project is no longer under active development. Much has changed since the summer of 2012 when BigVideo.js was launched. For more current information on implementing video backgrounds, check out these links:

- CSS Tricks - [Should I use a video as a background?](https://css-tricks.com/should-i-use-a-video-as-a-background/)
- Dudley Storey - [Create Fullscreen HTML5 Page Background Video](http://thenewcode.com/777/Create-Fullscreen-HTML5-Page-Background-Video)
- [Vide](http://vodkabears.github.io/vide/) - Easy as hell jQuery plugin for video backgrounds

If you are interested in taking over the project, ping me at <a href="https://twitter.com/johnpolacek">@johnpolacek</a></p>


## Installation
If you're using [Bower](http://bower.io) (and you should be!) installing BigVideo and its dependencies is simply:

```
bower install BigVideo.js
```

This downloads and installs BigVideo to the ``bower_components`` folder. Add to your page the usual way with script tags, or using [RequireJS](#requirejs).

If you'd rather download things manually, you can grab the latest zip from that lovely button on the right ([or this link](https://github.com/dfcb/BigVideo.js/archive/master.zip)). You will also need the dependencies:

* [Video.js 3.2 or higher](http://www.videojs.com/)
* [jQuery 1.7.2 or higher](http://jquery.com/download)

Additionally, if you are using image functionality:
* [jQuery UI slider 1.8.22 or higher](http://jqueryui.com/download/#!components=1110000000000000100000000000000000)
* [imagesloaded 2.1.1 or higher](http://desandro.github.io/imagesloaded/) 

## Options
The following are defaults on initialization:
``` js
    var BV = new $.BigVideo({
        // If you want to use a single mp4 source, set as true
        useFlashForFirefox:true,
        // If you are doing a playlist, the video won't play the first time
        // on a touchscreen unless the play event is attached to a user click
        forceAutoplay:false,
        controls:false,
        doLoop:false,
        container:$('body'),
        shrinkable:false
    });
```

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
		"BigVideo": "bower_components/BigVideo.js/lib/bigvideo",
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


* * *
The MIT License (MIT)
Copyright © 2012 John Polacek

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
