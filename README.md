# Create-MQTT-server-on-ubuntu-
Create MQTT server on ubuntu 



ChatGPT
To install an MQTT server on Linux Ubuntu, you can use Mosquitto, which is an open-source MQTT broker that implements the MQTT protocol versions 3.1 and 3.1.1. Here's how you can install Mosquitto on Ubuntu:

Update Package Lists: Ensure your package lists are up-to-date by running:
 
    >sudo apt update
Install Mosquitto Broker: Install the Mosquitto broker package by running:
 
    >sudo apt install mosquitto
This command installs the Mosquitto MQTT broker along with its dependencies.

Start Mosquitto Service: After installation, the Mosquitto service should start automatically. However, if it doesn't, or if you need to restart it for any reason, you can do so using:
 
    >sudo systemctl start mosquitto
Enable Mosquitto Service (Optional): If you want Mosquitto to start automatically every time the system boots, enable it using:
 
    >sudo systemctl enable mosquitto

## Verify Mosquitto Installation: 
You can verify that Mosquitto is running correctly by subscribing to a test topic. Open two terminal windows and in one, subscribe to a test topic  
     
     >mosquitto_sub -h localhost -t test

## In the second terminal, publish a message to the same topic using:

    >mosquitto_pub -h localhost -t test -m "Hello, MQTT!"
    
You should see the message "Hello, MQTT!" appear in the terminal where you subscribed to the topic.

That's it! You now have a Mosquitto MQTT broker installed and running on your Ubuntu system. You can configure it further as needed for your use case.
