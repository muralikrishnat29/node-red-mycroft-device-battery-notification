# node-red-mycroft-device-battery-notification 

This a very primitive module to demonstrate the flexibility of node-red. 

Here node-red flow executes on an edge IOT device to get battery status

Here the edge device used is an Android Mobile. The status is informed to a raspberry-pi where Mycroft an open source assistant is deployed.

Node-red is low level flow based programming tool that can be programmed using a browser.

Mycroft is open source voice assistant that can be deployed in variety of devices.

Communication to mycroft is established through its Messagebus i.e. through a WebSocket port

To make an android mobile capable of running node red and get some data, we need Termux, Termux API and related packages.

## Links and References:

1. [Termux](https://termux.com/)
2. [Termux API](https://wiki.termux.com/wiki/Termux:API)
3. [Node Red on Android](https://nodered.org/docs/getting-started/android)
4. [Picroft](https://mycroft-ai.gitbook.io/docs/using-mycroft-ai/get-mycroft/picroft)
5. [Mycroft](https://mycroft.ai/)

## Steps:
1. Follow links 1 and 2 and install Termux, Termux API and related packages
2. Install node-red on Android by following link 3
3. Decide the device to deploy mycroft and follow link 4 or 5 
4. After deploying mycroft, get the IP Address of the device
5. From this repo, copy the raw text of the file 'MobileFlow.txt'
6. Open node-red console module either in the same device's browser or different device's browser connected in the same network through the link http://localhost:1880 or http://<IP_Address_Of_Edge_Device>:1880/
7. In the browser working palette, find menu option. Click Import. In the dialog box, select clipboard option and paste the clipboard contents. 
8. Double click WebSocket node and modify IP_Address_Of_Mycroft_Deployed_Device to the one obtained in step 3. If same device. put 'localhost'
9. Click Deploy
10. When deployed, the WebSocket node should say 'Connected'. Else, the flow need to be verified
11. Adjust the threshold of battery in Switch node to the level you need. Now it is 70.
12. Redeploy and observe that after the mobile battery reaches below the threshold level mycroft instructs to plug the charger.



