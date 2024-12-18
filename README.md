# Barcode reader widget

This repository contains a Thingworx widget allowing reading of barcodes within the browser. Both file inputs, as well as modern webcam grabbing is supported.
The underlying technology behind this widget is [QuaggaJS2](https://github.com/ericblade/quagga2).
QuaggaJS is a barcode-scanner entirely written in JavaScript supporting real- time localization and decoding of various types of barcodes such as *EAN*, *CODE 128*, *CODE 39*, *EAN 8*, *UPC-A*, *UPC-C*, *I2of5*, *2of5*, *CODE 93* and *CODABAR*. The library is also capable of using _getUserMedia_ to get direct access to the user’s camera stream. Although the code relies on heavy image-processing even recent smartphones are capable of locating and decoding barcodes in real-time.

## How to use it

By default, this is a non-reposive widget, with a text input that can be customized via CSS and a button. The wodget can also be completely hidden, and the `StartDetection` service can be used to start the detection based on external events.
The widgets offers two functioning modes, driven by the `Mode` widget property. This modes dictate what happens when clicking on the button, or when triggering the `StartDetection` service.

* Live video: a popup is automatically opened and the device camera is used to directly scan for barcodes. The camera input also includes indicators of detected codes and upon succesful detection, the popup is closed, and the input is updated to the barcode detected. The popup also offers controls for the flashlight of the device (if available).
* File input: a file dialog opens allowing the user to select a photo. Depending on the used device, this can use the camera app to take a new photo.

To understand most of the widget properties, either read the description or go to the library [website](https://serratus.github.io/quaggaJS/#configuration).

## Building and publishing

The following commands allow you to build and compile your widget:

* `npm run build`: builds the production version of the widget. Creates a new extension zip file under the `zip` folder. The production version is optimized for sharing and using in production enviroments.
* `npm run upload`: creates a build, and uploads the extension zip to the thingworx server configured in `package.json`. The build is created for developement, with source-maps enabled.
* `npm run watch`: watches the source files, and whenever they change, do a build.

# Authors

Petrisor Lacatus - IOT Presales Engineer , Romania CoE Team



# Disclaimer
By downloading this software, the user acknowledges that it is unsupported, not reviewed for security purposes, and that the user assumes all risk for running it.

Users accept all risk whatsoever regarding the security of the code they download.

This software is not an official PTC product and is not officially supported by PTC.

PTC is not responsible for any maintenance for this software.

PTC will not accept technical support cases logged related to this Software.

This source code is offered freely and AS IS without any warranty.

The author of this code cannot be held accountable for the well-functioning of it.

The author shared the code that worked at a specific moment in time using specific versions of PTC products at that time, without the intention to make the code compliant with past, current or future versions of those PTC products.

The author has not committed to maintain this code and he may not be bound to maintain or fix it.


# License
I accept the MIT License (https://opensource.org/licenses/MIT) and agree that any software downloaded/utilized will be in compliance with that Agreement. However, despite anything to the contrary in the License Agreement, I agree as follows:

I acknowledge that I am not entitled to support assistance with respect to the software, and PTC will have no obligation to maintain the software or provide bug fixes or security patches or new releases.

The software is provided “As Is” and with no warranty, indemnitees or guarantees whatsoever, and PTC will have no liability whatsoever with respect to the software, including with respect to any intellectual property infringement claims or security incidents or data loss.
