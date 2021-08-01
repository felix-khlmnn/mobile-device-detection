# mobile-device-detection
 This simple module allows you to find out whether a client of an http server you run is using a mobile device or not. Also, the module does not require any dependencies, as it only uses the preinstalled http module.

## Functionality
The function "checkIfMobile" returns a boolean. The value is "true", if the client is using a mobile device. 
All that needs to be passed into the function is the request of the client. Below you will find a demonstration of the module.

## Usage
```javascript
const http = require("http");
const mdd = require("mobile-device-detection");

http.createServer((req, res) => {
    console.log(mdd.checkIfMobile(req));
    res.end()
}).listen(8080);
```

This will result in two possible logs in the console:

```bash
true
```
This means that the requesting client is using a mobile device.
```bash
false
```
This means that the requesting client is not using a mobile device.

## Credit
This is not my code! As I stumbled upon the issue of mobile device detection myself, I found a snippet of code in this [DZone article](https://dzone.com/articles/mobile-device-detection-and) and decided to condense it down into an easy to find module.

## Contact
If you run in any problems, feel free to write me an [email](mailto:dixi050504@gmail.com?subject=About%20mobile-device-detection) or just add me on Discord (dixi0505#0135).
I hope that you'll find this module useful.