# Intro to C2

### Payload Types

**Stageless**
- contain the full C2 agent and will immediately call back to the C2 server, immediately beaconing

![e79d46d97f108842b9424ae5a134d2f8](https://user-images.githubusercontent.com/95729902/226146953-f27b8700-82fe-48b5-9c38-d944072f582d.png)

**Steps to Execute Stageless Payloads**

1) Victim downloads and executes the Dropper
2) Beaconing to the C2 Server begins


**Staged**
- Require a callback to the C2 server to download additional parts
- Easier to obfuscate code to bypass anti-virus
- Preferred method over stageless payloads because a small amount of code is needed to retrieve additional parts of the C2 agent

![e6127ac6a295a1d9b01444757f711084](https://user-images.githubusercontent.com/95729902/226147090-906ba5e9-3780-4703-9913-f9dbb36999d6.png)



**Steps to Execute Staged Payloads**

1) The Victim downloads and executes the Dropper
2) The Dropper calls back to the C2 Server for Stage 2
3) The C2 Server sends Stage 2 back to the Victim Workstation
4) Stage 2 is loaded into memory on the Victim Workstation 
5) C2 Beaconing Initializes, and the Red Teamer/Threat Actors can engage with the Victim on the C2 Server.


### Domain Fronting

- Domain Fronting is a technique used to hide C2 frameworks in plain sight
- It utilizes a known good host to communicate with the C2 server

![cd1ea19e9e0d7bef0d8ec6615061335b](https://user-images.githubusercontent.com/95729902/226148093-81253987-fd5e-40c4-92b4-7e930a74026e.png)



