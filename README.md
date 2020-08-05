![SuperBlaster Logo](https://github.com/evScript-labs/SuperBlaster/blob/master/logo.png?raw=true)
# SuperBlaster : ESP8266 based infrared Hub

### Introduction
SuperBlaster provides a simple REST Interface to learn and send saved commands to infrared devices, thus enabling them to be linked with smart home applications.

### REST Interface


#### 🔍 List all learned commands
SuperBlaster saves all learned commands on the ESP8266, in order to get a list of all learned commands, send a HTTP request to

``
GET -> http://<ESP8266-address>/
``

#### 💡 Learning new commands

To learn a new command simply send a HTTP GET request like this.

``
GET -> http://<ESP8266-address>/learn?id=<Unique Identifier>&name=<Command Name>
``

#### ✉️ Sending learned commands

In order to send a command, send a HTTP GET request like the example below 

``
GET -> http://<ESP8266-address>/send?id=<Unique Identifier>
``

#### ❌ Delete learned commands

If you wish to remove a command from SuperBlaster, send a HTTP GET request like this

``
GET -> http://<ESP8266-address>/delete?id=<Unique Identifier>
``

#### ☠️ Delete ALL learned commands (Reset)

To reset all commands and perform a factory reset, send the following HTTP GET request

``
GET -> http://<ESP8266-address>/reset
``
