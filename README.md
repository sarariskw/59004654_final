<b>1. Dowload Software  </b>

 <a href="https://www.arduino.cc/en/software"><img src="https://www.arduino.cc/wiki/849deddaf8daab4ca3dd88761cc1c368/ArduinoAPP-01.svg" alt="image" border="0"></a>

<b>2. prepare Hardwares</b>

	- esp32
	- Soil Moisture Sensor
	- Relay Module 5V 
	- water pump
	- LED grow ligh

<b>3.When you get firmware.ino file ,Open it in Arduino ISE</b>

<b>4.In firmware.ino file,You have to change some part of them to be your data.</b>

	//Wi-Fi settings
	const char* ssid = " YOUR WIFI NAME";
	const char* password = " WIFI PASSWORD ";

	// MQTT INFORMATION ,You can get this information by creating an instant from the mqtt broker.
	const char* topic = " <<YOUR MQTT TOPIC NAME>> ";
	#define mqtt_server " <<YOUR MQTT SERVER>>"
	#define mqtt_port <<YOUR MQTT port>>
	#define mqtt_user " <<YOUR MQTT user>> "
	#define mqtt_password  " <<YOUR MQTT PASSWORD>> "

<b>5.Connect the hardware as declared in the code.</b>

	int Relay1 = 1;       //led at pin 1
	int pumpPin2 = 2;     //Water pump at pin 2
	int analogPin = A0;   //Soil Moisture Sensor at pin A0

<b>6.Check your connection (Wifi/MQTT) that you have connected.</b>

<b>7.Upload the firmware to esp32</b>

<img src="https://i.ibb.co/RHcHkQx/upload.png" alt="upload" border="0">

<b>8.You can send a message from MQTT to Hardware >> go to Websocket and send a message.if you send "on" LED will turn on.
if you send "off",LED will turn off.</b>

<img src="https://i.ibb.co/1Q95pHm/send.png" alt="send" border="0">

<b>9.For Node-red "server.json" file you must install node-red on your computer before. follow these step</b>

		-open CMD and input command
	
		for window >> npm install -g --unsafe-perm node-red  
		for ios    >> sudo npm install -g --unsafe-perm node-red		
<img src="https://i.ibb.co/QCQdXc2/noderednpmi.png" alt="noderednpmi" border="0">
		
<b>10.so you can run node-red by this command  </b>
	
	>> node-red
<img src="https://i.ibb.co/th4Jmy2/runnodered.png" alt="runnodered" border="0">

<b>11.you will get a link to connected to broker that you can open it in browser.</b>
<img src="https://i.ibb.co/SXdwH1z/getlink.png" alt="getlink" border="0">

<b>12.when you open it on browser you can import json file from your computer.</b>
<img src="https://i.ibb.co/NWSs4PY/import.png" alt="import" border="0"></a>

<b>13.then deploy it.</b>

<b>14.it will signal for you that it have connected with MQTT broker and serial port.</b>
<img src="https://i.ibb.co/hR3cYd6/connected.png" alt="connected" border="0">

<b>15.you can open the dashbroad on node-red.</b>

<img src="https://i.ibb.co/s5F9j78/dash.png" alt="dash" border="0">


<h1>Here is my project picture</h1>
<img src="https://i.ibb.co/vZs1p9q/image.jpg" alt="image" border="0">
