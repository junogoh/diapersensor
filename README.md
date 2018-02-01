# diapersensor
A sample Azure IoT Edge module that periodically sends simulated deviceID, poop reading, timestamp to Azure IoT Hub.

Install required packages.

    npm install azure-iot-device azure-iot-device-mqtt@latest --save
    npm install node-datetime --save
    npm install minimist --save
    
Replace your device id and connection string in config.json file.

    {
        "deviceId" : "D0001",
        "connectionString" : "HostName=yourhost.azure-devices.net;DeviceId=D0001;SharedAccessKey=yourshareaccesskey"
    }

Now start to program to send the messages to Azure IoT Hub.

    node index.js
    
You will see the logs as below.

    Connection String:HostName=yourhost.azure-devices.net;DeviceId=D0001;SharedAccessKey=yourshareaccesskey
    Device ID:D0001
    Client connected
    Sending message: {"deviceId":"D0001","sensor":"diaper","poop":true,"timestamp":"2018-02-02 01:00:33"}
    send status: MessageEnqueued
    Sending message: {"deviceId":"D0001","sensor":"diaper","poop":true,"timestamp":"2018-02-02 01:00:43"}
    send status: MessageEnqueued
    Sending message: {"deviceId":"D0001","sensor":"diaper","poop":true,"timestamp":"2018-02-02 01:00:53"}
    send status: MessageEnqueued

