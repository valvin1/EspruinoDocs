<!--- Copyright (c) 2015 Gordon Williams, Pur3 Ltd. See the file LICENSE for copying permission. -->
SeeedStudio Grove System
=====================

* KEYWORDS: SeeedStudio,Grove,System


Wiring
-----

When using the [Arduino adaptor shield](/ArduinoPico) on the Pico, just plug the Grove Arduino Shield on top of it.
A direct Grove Pico adaptor will be available soon as well.

Otherwise, you need to wire each module up to GND, VCC, and to signal wires on the Pico. The connections should be written on the board. If it specifies `SDA`/`SCL`, make sure you use pins on the Pico that can handle [[I2C]].

Software
-------

If you're using the [Arduino adaptor shield](/ArduinoPico) then you can easily use the [[GrovePico.js]] module to get the correct pins. Simply use the name written on the Grove adaptor. For instance for a button connected to `D4`:

```
var grove = require("GrovePico");
new (require("GroveButton"))(grove.D4, function(e) {
  if (e.state) console.log("Pressed");
  else console.log("Released");
});
```

If you've wired up a grove module manually, just put the 2 pins you used in an array, and use that instead:

```
new (require("GroveButton"))([A0,A1], function(e) {
  if (e.state) console.log("Pressed");
  else console.log("Released");
});
```

Button
-----

* APPEND_JSDOC: GroveButton.js

Buzzer
-----

* APPEND_JSDOC: GroveBuzzer.js

Touch
----

* APPEND_JSDOC: GroveTouch.js

Rotation
-------

* APPEND_JSDOC: GroveRotation.js

Light Sensor
----------

* APPEND_JSDOC: GroveLightSensor.js

Temperature
----------

* APPEND_JSDOC: GroveTemperature.js

Relay
----

* APPEND_JSDOC: GroveRelay.js

LCD RGB
------

* APPEND_JSDOC: GroveLCDRGB.js
