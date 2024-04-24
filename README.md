# Cisco-Packet-Tracer
Set up home lab

# Setting Up a Home Network with Cisco Packet Tracer

<img width="761" alt="image" src="https://github.com/MiguelAngelHorta/Cisco-Packet-Tracer/assets/106134627/d3c365ab-7002-4609-865b-a7ca0d8234ab">


## 1. Obtain Cisco Packet Tracer
- Visit [Cisco's official website](https://skillsforall.com/learningcollections/cisco-packet-tracer?courseLang=en-US&utm_source=netacad.com&utm_medium=referral&utm_campaign=packet-tracer&userlogin=0![image](https://github.com/MiguelAngelHorta/Cisco-Packet-Tracer/assets/106134627/30d5ae1d-afe0-42c5-b342-347696194753)
) to download Cisco Packet Tracer.
- Follow the installation instructions provided by Cisco to set up the software on your computer.

## 2. Deploy Devices
- Open Cisco Packet Tracer and create a new project.
- Drag and drop the required devices from the device list onto the workspace.
  - For wireless devices, select a suitable wireless router model.
  - For endpoints, include a laptop and a PC.
  - Server
  - Cable modem
  - Cloud Provider

## 3. Configure Router
- Access the configuration interface of the wireless router by double-clicking on it.
- Configure the following settings:
  - Set the IP address to `192.168.0.1` with a subnet mask of `255.255.255.0`.
  - Specify the maximum number of users (e.g., 50).
  - Set a static DNS server (e.g., `208.165.200.255`).
  - <img width="696" alt="image" src="https://github.com/MiguelAngelHorta/Cisco-Packet-Tracer/assets/106134627/3c16e6e6-7881-48c9-bae5-b2375722aef6">
  - Assign a wireless network name (SSID) like "HomeNetwork".
  - <img width="714" alt="image" src="https://github.com/MiguelAngelHorta/Cisco-Packet-Tracer/assets/106134627/8919d9bc-8f89-4437-b33b-35102696f68b">
- Modify the laptop settings:
  - Turn off the laptop, replace the network card with a WPC300N card, and then turn it back on.
  - <img width="676" alt="image" src="https://github.com/MiguelAngelHorta/Cisco-Packet-Tracer/assets/106134627/8775bbe6-3105-47e7-8a48-b7a7501d3e32">
  - Connect the PC wirelessly to the router and ensure it's connected to the "HomeNetwork".
  - <img width="403" alt="image" src="https://github.com/MiguelAngelHorta/Cisco-Packet-Tracer/assets/106134627/e9bee7de-73f5-402b-8b8b-362f06306530">
  -  <img width="587" alt="image" src="https://github.com/MiguelAngelHorta/Cisco-Packet-Tracer/assets/106134627/9a86bff7-c8ef-4f1c-9461-828c26aa7285">
  -Laptop is now connected to the router
  - <img width="451" alt="image" src="https://github.com/MiguelAngelHorta/Cisco-Packet-Tracer/assets/106134627/2ff54e53-b6eb-46ff-8ce3-117aa4cc7305">
- Configure the laptop's IP settings:
  - Navigate to the laptop's network settings and select IP configuration.
  - <img width="690" alt="image" src="https://github.com/MiguelAngelHorta/Cisco-Packet-Tracer/assets/106134627/02afb9e2-449c-4fe0-997c-ddf915dc46d5">
  - Set DHCP for the gateway/DNS IPv4.
  - <img width="681" alt="image" src="https://github.com/MiguelAngelHorta/Cisco-Packet-Tracer/assets/106134627/dfb1c589-d070-468d-aadd-a03d00d8f0ad">
  - <img width="688" alt="image" src="https://github.com/MiguelAngelHorta/Cisco-Packet-Tracer/assets/106134627/cb30d2de-1844-4350-8ee3-f8e1c3de220e">
- Confirm the configuration by opening the Command Prompt on the desktop and running the command `ipconfig /all`.
  - <img width="477" alt="image" src="https://github.com/MiguelAngelHorta/Cisco-Packet-Tracer/assets/106134627/01ea1c98-0cc2-457e-8c82-1e13d1fa8edf">

## 4. Configure Cloud PT
- Connect the cable modem to the cloud device using a coaxial cable (port 0 to coaxial 7).
- Connect the cloud device to the server using a straight-through copper cable (Ethernet 6 to Fast Ethernet).
  - Access the configuration interface of the cloud device.
  - Ethernet 6 is changed to cable
    - <img width="593" alt="image" src="https://github.com/MiguelAngelHorta/Cisco-Packet-Tracer/assets/106134627/9ee8f398-3eb0-4947-a42d-a90023e29167">
  - Add coaxical7 to ethernet 6
    - <img width="675" alt="image" src="https://github.com/MiguelAngelHorta/Cisco-Packet-Tracer/assets/106134627/64a59b23-0149-42fd-aa03-8a817a5375a5">



## 5. Configure Cisco.com Server
- Access the configuration interface of the server device.
- Configure the FastEthernet settings for the server.
  - <img width="664" alt="image" src="https://github.com/MiguelAngelHorta/Cisco-Packet-Tracer/assets/106134627/25a998c3-ba53-4584-a25a-49da70761734">
- Set global settings as required.
  - <img width="665" alt="image" src="https://github.com/MiguelAngelHorta/Cisco-Packet-Tracer/assets/106134627/06b19021-e3b2-4efa-9b08-fb6397970dcc">
- Configure DHCP for the server.
  - <img width="664" alt="image" src="https://github.com/MiguelAngelHorta/Cisco-Packet-Tracer/assets/106134627/f53057a5-f9ce-4cb5-bd0c-91f2c260dded">
- Configure DNS for the server.
  - <img width="662" alt="image" src="https://github.com/MiguelAngelHorta/Cisco-Packet-Tracer/assets/106134627/1959c873-01cb-48b5-9c4d-518eea5fe3c8">
- Test connectivity:
  - Go to the PC and open the Command Prompt.
  - Use commands like `ipconfig /release` and `ipconfig /renew` to manage IP address configurations.
  - Ping the Cisco server using the command `ping cisco.com` to test reachability and measure round-trip time for network communication.
  - <img width="338" alt="image" src="https://github.com/MiguelAngelHorta/Cisco-Packet-Tracer/assets/106134627/a910d30f-0161-4897-a296-c808b90ea0ae">


## 6. General
- Save your project in Cisco Packet Tracer to preserve your progress.
