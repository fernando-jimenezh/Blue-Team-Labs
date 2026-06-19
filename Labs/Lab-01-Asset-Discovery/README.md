# Lab 01 - Asset Discovery

## Objective

Identify and classify assets present in a local network using active discovery techniques.

## Environment

- Windows 11 Host
- Kali Linux VM (Bridge Mode)
- Home Network

## Tools

- Nmap
- ARP
- Tcpdump

## Methodology

1. Network discovery
2. Host identification
3. Service enumeration
4. Operating system fingerprinting
5. Asset classification

## Commands Used

```bash
nmap -sn 192.168.1.0/24
```

```bash
nmap -sV 192.168.1.0/24
```

```bash
nmap -O <IP>
```

```bash
nmap --script broadcast-upnp-info
```

## Findings

### Router

- Fiberhome Router
- Gateway device

### Smart TV

- UPnP enabled
- DLNA services detected

### Android TV / Fire TV

- ADB service exposed on TCP 5555

### DVR / NVR

- RTSP service available
- Web administration interface exposed

## MITRE ATT&CK

### T1046 - Network Service Discovery

Discovery activity was performed to identify network assets and exposed services.

## Conclusion

A complete inventory of network assets was obtained, including infrastructure, multimedia devices and embedded systems. Several exposed services were identified and documented for future detection and threat hunting exercises.
