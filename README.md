jQuery Video Controller
==============
This video plugin for jQuery allows you to controll **HTML5,** **Youtube** and **Vimeo** Videos with the same functions and the same syntax.

## Dependencies
* <a href="http://jquery.com/" target="_blank">jQuery 1.9+</a>

## Installation
* Download the file `jquery.video.min.js`
* Upload it to your server (e.g. `/js/` folder)
* Embed the file in your html code: `<script src="/js/jquery.video.min.js"></script>`

## Use

Each of the following functions can be triggered on **one** or **multiple** videos.

### Initialize video(s)
Initializes the video(s) and change default settings if necessary.
```javascript
$('.video').video();
// or
$('.video').initVideo();
```

### Play videos
Plays or resumes the video(s).
```javascript
$('.video').playVideo();
// or
$('.video').video('play');
```

### Pause videos
Pauses the video(s) at the current position.
```javascript
$('.video').pauseVideo();
// or
$('.video').video('pause');
```

### Stop videos
Stops the video(s). HTML5 and Vimeo videos will stop and resetted to the initial state. Youtube videos will jump to the end of the video (and trigger de finish event).
```javascript
$('.video').stopVideo();
// or
$('.video').video('stop');
```
### Restart videos
Jump to the beginning of the video(s) and restart playing.
```javascript
$('.video').restartVideo();
// or
$('.video').video('restart');
```
### Mute videos
Mute the video(s)
```javascript
$('.video').muteVideo();
// or
$('.video').video('mute');
```
### Unmute videos
Unmute the video(s). The volume of vimeo videos will be set to 1 (max).
```javascript
$('.video').unmuteVideo();
// or
$('.video').video('unmute');
```
### Jump to position
Jumps to a defined position (seconds) in the videos.
```javascript
$('.video').seekToVideo(30);
// or
$('.video').video('seekTo', 30);
```
### Add event to video
Adds an event to a video.
```javascript
$('.video').addVideoEvent('play', onPlay);
// or
$('.video').video('addVideoEvent', 'play', onPlay);
```
### Remove event to video
Removes an event from a video.
```javascript
$('.video').removeVideoEvent('play');
// or
$('.video').video('removeVideoEvent', 'play');
```
## Events
### onReady
Triggers if a video is loaded and ready.
```javascript
$('.video').addVideoEvent('ready', onReady);
// or
$('.video').video('addVideoEvent', 'ready', onReady);
```
### onPlay
Triggers on play or resume.
```javascript
$('.video').addVideoEvent('play', onPlay);
// or
$('.video').video('addVideoEvent', 'play', onPlay);
```
### onPause
Triggers on pause.
```javascript
$('.video').addVideoEvent('pause', onPause);
// or
$('.video').video('addVideoEvent', 'pause', onPause);
```
### onFinish
Triggers has reached the end and is finished. The stop method on Youtube Videos will trigger this event too.
```javascript
$('.video').addVideoEvent('finish', onFinish);
// or
$('.video').video('addVideoEvent', 'finish', onFinish);
```
### onDestroy
Triggers if the video is destroyed.
```javascript
$('.video').addVideoEvent('destroy', onDestroy);
// or
$('.video').video('addVideoEvent', 'destroy', onDestroy);
```
## Todo
* more events and methods
* settings (autoplay etc.)

## Changelog
##### v0.1.0 (2015-06-10)
Initial release