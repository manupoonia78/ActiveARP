
# ARP Poisoning Defender

Active ARP protects your PC against **Man-In-The-Middle (MITM)** attacks. This is a script written in C to provide protection against malicious ARP attacks, which changes the gateway's MAC Address in the ARP table of a victim's PC.

# Installation and build
Active ARP needs arptables and libpcap-dev to run, so just install them:
```
sudo apt-get install arptables libpcap-dev
```

There's a pre-built executable in the builds folder, or build it yourself:

To build:
* Run `compile_arppd_linux`

OR

* Go in the main directory
* Run:
```
gcc -o builds/defender-win64 src-win64/defender.c -lpcap -pthread
```

# Malicious ARP Packets
When the Active ARP will detect a malicious ARP Packet, it will look like this:

![image](https://i.imgur.com/OiRGz9E.png)

