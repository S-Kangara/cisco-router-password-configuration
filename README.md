# Cisco Packet Tracer Lab – Router Password Encryption

## 📌 Overview
This is a Cisco Packet Tracer lab demonstrating basic router configuration, including hostname setup, enable password configuration, and password encryption (`service password-encryption`) on two Cisco 1941 routers (R1 and R2).

## 🖥️ Topology
- **R1** — Cisco 1941 Router
- **R2** — Cisco 1941 Router
- Connected via **GigabitEthernet0/0** interfaces using a straight-through cable

## 🎯 Lab Objectives
1. Connect R1 and R2 via their GigabitEthernet0/0 interfaces
2. Set hostnames according to the network diagram (R1 and R2)
3. Set the enable password on each router to `cisco`
4. View the password in the running configuration and check if it's encrypted
5. Enable password encryption (`service password-encryption`) on each router
6. View the running configuration again to confirm encryption
7. Disable password encryption on each router
8. View the running configuration once more to observe the behavior after disabling encryption

## 🔑 Key Learning Outcome
Once a password is encrypted using `service password-encryption`, disabling the command with `no service password-encryption` does **not** decrypt it again. The password remains encrypted in the running configuration — the command only prevents *future* passwords from being encrypted.

## ⚙️ Configuration Commands Used

```bash
# Hostname configuration
Router(config)#hostname R1

# Enable password
R1(config)#enable password cisco

# View running config
R1#show running-config

# Enable password encryption
R1(config)#service password-encryption

# Disable password encryption
R1(config)#no service password-encryption
```

## 📂 Files in this Repository
- `lab.pkt` — The Cisco Packet Tracer file for this lab
- `README.md` — This documentation file

## 🛠️ Tools Used
- Cisco Packet Tracer

## 📝 Notes
- The enable password used in this lab (`cisco`) is for lab/practice purposes only. Never use weak or default passwords in a real production network.
- Consider using `enable secret` instead of `enable password` in real-world scenarios, since `enable secret` uses stronger MD5/Type 5 (or better) hashing by default.
