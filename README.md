# Countdown.js [![Build Status](https://travis-ci.org/gumroad/countdown.js.png)](https://travis-ci.org/gumroad/countdown.js)


![image](https://github.com/user-attachments/assets/380be6ec-098b-49ab-b82e-2d8a4ee400ee)

Countdown.js is a library that allows developers to set countdowns for any kind of interaction.  For example, if you would
like to submit a form, Countdown.js allows you to set a 5 second countdown and give the user a chance to cancel the
submission. You can see it in action by opening the included `simple-timer.html` file in your browser.

## Installation

If you use bower:
```
bower install countdown.js
```

Otherwise, you can download it from [here](https://raw.github.com/gumroad/countdown.js/master/lib/countdown.js).

## API

### new Countdown(duration, onTick, onComplete)

Begins a countdown.  After `duration` time has passed, the function `onComplete `will be executed.  Every second, the `onTick`
function will be executed.  

Example:

```javascript
var countdown = new Countdown(5, function(seconds) {
  console.log(seconds); //log the number of seconds that have passed
}, function() {
   console.log("Countdown complete!") //log that the countdown has complete
});
```

### abort()

Terminates countdown.  

Example:

```javascript
countdown.abort();
```

### getRemainingTime()

Returns remaining time in seconds.

Example:

```javascript
countdown.getRemainingTime(); //=> 4
```

## Example

Open `simple-timer.html` in your browser to see a beautiful 10-second countdown timer demonstration. 

For local development, you can serve it using a local server like Live Server:
```
http://127.0.0.1:5500/simple-timer.html
```

The demo features:
- ⏱️ Clean 10-second countdown timer
- 🎨 Dark, cinematic design with glowing effects  
- 🎮 Interactive controls (click or keyboard)
- ✨ Smooth animations and particle effects
- 🚨 Visual urgency indicators for final seconds
- 🎉 Celebration effects on completion

This demo showcases the core Countdown.js API:
```javascript
new Countdown(10, 
    function onTick(secondsLeft) {
        // Updates display every second
        updateTimerDisplay(secondsLeft);
    },
    function onComplete() {
        // Triggers completion effects
        showCelebration();
    }
);
```

## Contribute

Install development dependencies
```
npm install
```

## Test

```
npm test
```
