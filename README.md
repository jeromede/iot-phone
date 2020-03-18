Device simulation in a mobile browser
-------------------------------------

Will detect acceleration along and rotation around the x, y, z axis.

See specification documents at <https://w3c.github.io/deviceorientation> and <https://developer.mozilla.org/en-US/docs/Web/API/DeviceMotionEvent>

![Axis](img/axis.png)

Configuration:

* `js/config_dev.js` : change with your IoT Platform device configuration

Files:

* `index.html` : load this in the browser as a local file (file://)
* `lib/iotf-client-bundle.js` : IBMIoTF from <https://github.com/ibm-watson-iot/iot-nodejs>
* `js/config_dev.js` : change with your own IoT Platform configuration
* `js/main_dev.js` : main program

The main program:

* connects when `index.html` is loaded, and turns the background to white
* sends "accelerationIncludingGravity" events
* subscribes to all commands
* if the received command is
  * "alert": change the background to red
  * "clear": change back the background to white
* disconnects after 20 seconds, the background turns to light blue

Reload the page to reconnect.

Android, tested with [Firefox](https://play.google.com/store/apps/details?id=org.mozilla.firefox):

* copy the folder anywhere and navigate from <file:///storage> until you reach `index.html`

iPhone, tested with [FileApp](http://fileapp.com/):

* copy the folder (use USB cable, or Wifi and ftp —see documentation)
* open the folder
* click index(.html)
* it will open in a browser

