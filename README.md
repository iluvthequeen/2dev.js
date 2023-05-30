# 2dev.js
2dev.js is a 2D game development library for HTML5 Canvas. I originally started developing this library so I could create my games quickly without having to redo any of the math for collision logic. But I kept adding new functions to the library and decided to publish it. This library is very simple and is intended to make game development on Canvas as easy as possible. It is also not a complete library yet, as this is only version 1. But, I will be updating it very often, so be sure to check frequently for new features.
<br/>
# Tutorial
### NOTE: The origin of any object's position is always the center.
### Canvas Variables and Functions
```javascript
const myCanvas = new Canvas(width, height); // Creates a new canvas

// Canvas variables
myCanvas.width, myCanvas.height    // Get canvas width and height
myCanvas.HTML                      // Get the canvas element and DOM properties
myCanvas.Mouse.x, myCanvas.Mouse.y // Get the mouse x and y position on the canvas

// Event functions
// Use 'K_' followed by the event's code in all caps to refer to a key
myCanvas.On.KeyDown(key, func, shouldPreventDefault); // Adds a new key down event to the canvas
myCanvas.On.KeyUp(key, func, shouldPreventDefault);   // Adds a new key up event to the canvas
myCanvas.On.MouseDown = function () {                 // Adds a new mouse down event to the canvas
  // do something
}
myCanvas.On.MouseUp = function() {                    // Adds a new mouse up event to the canvas
  // do something
}

// Drawing functions
myCanvas.Fill(color);    // Fills the canvas with a solid color
myCanvas.Draw(objects);  // Draws any number of objects to the canvas. The first objects
                         // given will be drawn first. Any objects must be drawn to the canvas using this function
myCanvas.Erase(objects); // Erases any number of objects from the canvas
myCanvas.Clear();        // Clears the canvas
```
### Images and Audio
```javascript
// Loading image and audio files
LoadImg(images);   // Loads any number of image files
LoadSound(sounds); // Loads any number of audio files

// Accessing loaded sounds
LoadedSounds[index];       // An array storing all loaded sounds
LoadedSounds[index].audio; // A property storing the HTML audio element
LoadedSounds[index].src;   // A property storing the audio file's source

// Creating image objects and playing sounds
Img(src, x, y, width, height); // Creates a new image object
PlaySound(src);                // Plays a sound
```
### Objects
```javascript
// Creating objects
Rect(x, y, width, height, color);        // Creates a new rectangle object
Circle(x, y, radius, color);             // Creates a new circle object
Line(x1, y1, x2, y2, color);             // Creates a new line object
Text(text, font, fontSize, x, y, color); // Creates a new text object
```
