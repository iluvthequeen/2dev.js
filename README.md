**I'm still working on version 1 of 2dev.js. It will be uploaded to this page when it is finished.**
<br/>
# 2dev.js
2dev.js is a 2D game development library for HTML5 Canvas. I originally started developing this library so I could create my games quickly without having to redo any of the math for collision logic. But I kept adding new functions to the library and decided to publish it. This library is very simple and is intended to make game development on an HTML5 Canvas as easy as possible. This is not a complete library yet, as this is only version 1. But I will be updating it very often, so be sure to check back frequently for new features.
<br/>
# Tutorial
### NOTE: The origin of any object's position and rotation is always the center.
### Canvas Variables and Functions
```javascript
const myCanvas = new Canvas(width, height); // Creates a new canvas

// Canvas variables
myCanvas.width, myCanvas.height    // Get canvas width and height
myCanvas.HTML                      // Get the canvas element and DOM properties
myCanvas.Mouse.x, myCanvas.Mouse.y // Get the mouse position on the canvas

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
Img(src, x, y, width, height);           // Creates a new image object
Rect(x, y, width, height, color);        // Creates a new rectangle object
Circle(x, y, radius, color);             // Creates a new circle object
Line([x1, y1], [x2, y2], color);         // Creates a new line object
Text(text, font, fontSize, x, y, color); // Creates a new text object

// Image object properties
img.src = newSrc;             // Sets the source of the image. Make sure to load
                              // the image before drawing it to a canvas
img.x = newXPosition;         // Sets the x position of the rectangle
img.y = newYPosition;         // Sets the y position of the rectangle
img.width = newWidth;         // Sets the width of the rectangle
img.height = newHeight;       // Sets the height of the rectangle
img.color = newColor;         // Sets the color of the rectangle
img.velocityX = newVelocityX; // Sets the x velocity of the rectangle. This value
                              // is added to the rectangle's x position every frame
img.velocityY = newVelocityY; // Sets the y velocity of the rectangle. This value
                              // is added to the rectangle's y position every frame
img.SetPosition(x, y);        // Sets the position of the rectangle
img.GlideTo(x, y, timeInMs);  // Moves the rectangle to any position over a certain amount of time

// Rectangle object properties
rect.x = newXPosition;         // Sets the x position of the rectangle
rect.y = newYPosition;         // Sets the y position of the rectangle
rect.width = newWidth;         // Sets the width of the rectangle
rect.height = newHeight;       // Sets the height of the rectangle
rect.color = newColor;         // Sets the color of the rectangle
rect.velocityX = newVelocityX; // Sets the x velocity of the rectangle. This value
                               // is added to the rectangle's x position every frame
rect.velocityY = newVelocityY; // Sets the y velocity of the rectangle. This value
                               // is added to the rectangle's y position every frame
rect.SetPosition(x, y);        // Sets the position of the rectangle
rect.GlideTo(x, y, timeInMs);  // Moves the rectangle to any position over a certain amount of time
```
