# AzureSasTokenCreator
Generate a shared access token to send a message via REST to the Microsoft Azure IoT hub.

It is very easy to use a REST request to send a message to your Microsoft Azure IoT hub:
POST https://myiothub.azure-devices.net/devices/mydevice/messages/events?api-version=2016-02-03

However, the SharedAccessSignature (SAS) token must be provided as header field "Authorization".

To generate the SAS token using Java 8 the class AzureSasTokenCreator can be used. It is based on the Microsoft Azure IoT SDK for Java (https://github.com/Azure/azure-iot-sdk-java), but without the overhead. 

Important: You can find the device primary key in the Azure portal. Go to  youriothub  --> Devices --> yourdevice --> Primary key