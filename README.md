# reaction-time
Recreating reaction time app at humanbenchmark.com/tests/reactiontime

**Demo:** https://www.kdvuong.github.io/reaction-time

**How it works**

I began by creating 3 different div boxes, stacking on each other.
By changing the z-index value, I can manipulate which box to show on screen.

When the green box appears on screen,
```javascript 
var start = performance.now()
```

When the user clicks the green box, 
```javascript 
var elasped = performance.now() - start
```

**Notes**
Initially, the eventListener for user mouse click was ```onclick.```
However, when using ```onclick```, ```performance.now()``` will not be called until mouse click is up, causing a delay.
So to be more accurate, I changed the eventListener to ```onmousedown```.

