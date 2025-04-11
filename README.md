<p align="center">
  



<h1 align="center">Basic Router Configuration in Cisco Packet Tracer</h1>

<p align="center">
  This guide walks through the basic setup and configuration of a Cisco router in Packet Tracer, including hostname setup, interface configuration, and testing connectivity with end devices.
</p>

---

## 🧰 Tools and Technologies Used

- **Cisco Packet Tracer**
- **Cisco Routers & Switches**
- **PCs/End Devices**
- **Command Line Interface (CLI)**

## 💻 Environment Setup

- One router (e.g., `Router0`)
- One switch (e.g., `Switch0`)
- Two PCs (`PC0`, `PC1`)
- Ethernet cables for connectivity

---

## 🔧 Basic Configuration Steps

### Step 1: Connect Devices

- Use `Copper Straight-Through` cables to connect:
  - `Router0` (FastEthernet0/0) to `Switch0` (Fa0/1)
  - `PC0` to `Switch0` (Fa0/2)
  - `PC1` to `Switch0` (Fa0/3)

---

### Step 2: Configure Router (Router0)

Click the router, go to the CLI tab, enter configuration mode it will look something like this:

```bash
Router> enable
Router# configure terminal
Router(config)# hostname R1
R1(config)# interface fastethernet0/0
R1(config-if)# ip address 192.168.1.1 255.255.255.0
R1(config-if)# no shutdown
R1(config-if)# exit
R1(config)# exit
R1# write memory
```
### Step 3: Configure PCs

Click on each PC, go to Desktop > IP Configuration, and input:

For PC0: Example
- IP Address: `192.168.1.2`
- Subnet Mask: `255.255.255.0`
- Default Gateway: `192.168.1.1`

For PC1: Example
- IP Address: `192.168.1.3`
- Subnet Mask: `255.255.255.0`
- Default Gateway: `192.168.1.1`

### Step 4: Test Connectivity

On PC0, open the Command Prompt and type:

- `ping 192.168.1.1`     # Ping router
- `ping 192.168.1.3`     # Ping PC1

Successful replies indicate correct setup.

🧪 Final Notes
- Always remember to use no shutdown to activate router interfaces.
- Save your configuration using write memory or copy run start.
- Packet Tracer is a great tool to simulate real Cisco networking environments.


