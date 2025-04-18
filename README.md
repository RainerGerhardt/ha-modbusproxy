# Home Assistant AddOn Modbus Proxy second instance

Allows you to connect multiple clients to one single modbus server. Usally one modbus server only allows a single connection and denies any more clients. 

The addon is only tested and compatible with hassio supervisor. 

## Installation
[![Open your Home Assistant instance and show the add add-on repository dialog with a specific repository URL pre-filled.](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2FAkulatraxas%2Fha-modbusproxy)
- Add This [Repository](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2FAkulatraxas%2Fha-modbusproxy) (Or click Button above)
- Install ModBusProxy from the Add-On Store

## Configuration
- Stop all Clients that currently connect to the modbus server. The Server might need some time before another client (our proxy) can connect.
  - In case you are using solaredge-modbus in homeassistant you can change the server address here: /config/.storage/core.config_entries. 
- Before starting go to the configuration page and set the ip of your modbus server. 
- Start The Add-On
  - This may take a while on the first start as it builds the cointainer locally. If there is more interest ill switch to prebuild containters.
- Configure Your Clients to connect to your HA IP and choosen port.
- I recommend not to change the listenport in neither the network section nor the listenport. 

### Configuration Tab
<img width="382" alt="image" src="https://user-images.githubusercontent.com/103323/163730831-3b757097-c47f-4420-aebe-9fd357b12db4.png">

### Output after Start
<img width="935" alt="image" src="https://user-images.githubusercontent.com/103323/163732834-0ccc2bcd-94eb-4506-bdd1-5466fb82e76a.png">



## Mentions
This addon uses the modbus-proxy of tiagocoutinho:
- https://github.com/tiagocoutinho/modbus-proxy
