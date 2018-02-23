# esp8266-web-api
Rich API for building web application for ESP8266 modules

## Features
- Control digital and analog Pins
- Serial over realtime socket
- Debug serial passthrough
- Read and modify file system
- Upload files to SPIFS and SD Card
- Config power setting
- Config and connect to WiFi
- System status and variables
- Build with React

## Javascript API Usage

```js
ESP.IO.stat().then(stat => {})

ESP.IO.digitalRead(1).then(value => {})
ESP.IO.digitalWrite(1, true)

ESP.IO.analogRead(1).then(value => {})
ESP.IO.analogWrite(2, 768)

ESP.IO.on(1, 'change').then(handler)
ESP.IO.on(1, 'rise').then(handler)
ESP.IO.on(1, 'fall').then(handler)

ESP.WiFi.mode(ESP.WIFI_AP_STA)
ESP.WiFi.AP('ssid', 'password')
ESP.WiFi.scan().then(networks => {})
ESP.WiFi.join('ssid', 'password')

ESP.FS.list('/src').then(items => {})
ESP.FS.read('/src/app.js').then(content => {})
ESP.FS.write('/src/app.js', content)
ESP.FS.remove('/src/app.js')
ESP.FS.exists('/src/app.js')

ESP.SD.format()
ESP.SD.list('/MEDIA').then(items => {})
ESP.SD.read('/MEDIA/QBC001.mov').then(content => {})
ESP.SD.write('/MEDIA/QBC001.mov', content)
ESP.SD.remove('/MEDIA/QBC001.mov')
ESP.SD.exists('/MEDIA/QBC001.mov')
```

