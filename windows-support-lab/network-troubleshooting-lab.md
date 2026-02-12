# Network Troubleshooting Lab – IT Support Simulation

This document demonstrates practical network troubleshooting skills applied in a Help Desk / IT Support environment.

---

## Scenario 1 – User Has No Internet Access

### Reported Issue
User cannot access websites. Browser displays "No Internet".

### Step 1 – Check IP Configuration

Command used:
ipconfig

What to verify:
- Valid IPv4 address assigned
- No APIPA address (169.254.x.x)
- Default Gateway present
- DNS servers assigned

Explanation:
If the IP starts with 169.254.x.x, DHCP failed to assign an address.

---

### Step 2 – Test Network Connectivity

Commands used:
ping 8.8.8.8
ping google.com

Analysis:
- If ping to 8.8.8.8 works but google.com fails → DNS issue.
- If both fail → Possible gateway/router or ISP issue.
- If local gateway fails → Internal network issue.

---

### Step 3 – DNS Troubleshooting

Commands used:
ipconfig /flushdns
ipconfig /release
ipconfig /renew

Purpose:
- Clear DNS cache
- Request new IP from DHCP server
- Renew network configuration

---

### Step 4 – Advanced Diagnostics

Commands used:
tracert google.com
netstat -an

Purpose:
- tracert identifies where connection fails along the route.
- netstat verifies active connections and listening ports.

---

## Scenario 2 – Limited Connectivity (APIPA Address)

Symptoms:
User receives IP address 169.254.x.x

Diagnosis:
- DHCP server unreachable
- Network cable unplugged
- Router malfunction

Resolution Steps:
1. Restart router
2. Check physical connection
3. Renew IP configuration
4. Verify DHCP service

---

## Networking Knowledge Applied

- Understanding of DHCP and IP assignment
- DNS resolution process
- Basic routing concepts
- TCP/IP fundamentals
- Practical experience using Cisco Packet Tracer
- Basic router configuration and troubleshooting

---

## Tools Used

- Windows Command Prompt
- Cisco Packet Tracer (network simulation)
- Basic router troubleshooting concepts
