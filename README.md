# Ball Orientation Demo Web App by Allen Liu

I created a simple web app that utilizes orientation values from your phone (which are derived through sensor fusion of accelerometers, gryoscopes, geomagnetic field sensor, etc.) to control a ball moving into a bounded box.

## How I built it
### Reading Sensors
Device orientation is provided through the aptly named "deviceorientation" event which is already included in Javascript and does not require any external libraries. I use DeviceOrientationEvent.beta and DeviceOrientationEvent.gamma as the two axes required for the ball. Each tick, I update the ball's velocity in both directions based on the readings from the accelerometer.

### Creating Ball
The rendering and animation of the ball is largely handled by the move function which draws the ball based on the stored position state, updates the ball's position with velocity, and handle bound checking. The rectangle is a canvas object and the canvas object provides functions to draw like the the ball.

## Demo Video
[link](https://drive.google.com/file/d/1oPr4eg1q-roQTi6X0d16CKsSb9-Hje56/view?usp=sharing)

## Try it out
Link to demo (please access with phone and not safari): [https://aliuliu121.github.io/ballOrientationDemo/](https://aliuliu121.github.io/ballOrientationDemo/)

## References
Javascript Sensor Demo [link](https://sensor-js.xyz/demo.html)

Javascript Bouncing Ball Demo [link](https://www.geeksforgeeks.org/how-to-build-a-bounce-ball-with-html-and-javascript/)