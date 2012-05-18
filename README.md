*** ifvisible.js

Crosbrowser way to check if user is looking at the page or interacting with it.

Here are few examples:

```javascript

ifvisible.on("blur", function(){
	// example code here..
	animations.pause();
});

ifvisible.on("focus", function(){
	animations.resume();
});

```

ifvisible.js can handle visible states too such as being IDLE or ACTIVE on the page

```javascript

ifvisible.on("idle", function(){
	// Stop auto updating the live data
	stream.pause();
});

ifvisible.on("wakeup", function(){

	stream.resume();
});

```


You can set your smart intervals with ifvisible.js, if user is IDLE or not seeing the action it interval will automatically stop itself

```javascript

// If page is visible run this function on every half seconds
ifvisible.onEvery(0.5, function(){
    
	animateLogo();

});

```

