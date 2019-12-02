# node-red-mycroft-device-battery-notification 

This is a node-red project where node-red flow executes on an edge IOT device to get battery status

Here the edge device used is an Android Mobile. The status is informed to a raspberry-pi where Mycroft an open source assistant is deployed.

Node-red is low level flow based programming tool that can be programmed using a browser.

Mycroft is open source voice assistant that can be deployed in variety of devices.

Communication to mycroft is established through its Messagebus i.e. through a WebSocket port

To make an android mobile capable of running node red and get some data, we need Termux, Termux API and related packages.
