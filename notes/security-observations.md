# Security Observations

## 10.0.2.2

The host responded with four open TCP ports:

- TCP/135 – Microsoft Windows RPC
- TCP/445 – Microsoft-DS/SMB-related service
- TCP/5432 – PostgreSQL database
- TCP/9080 – HTTP response observed, but the exact service was not identified by Nmap

### Security considerations

TCP/135 and TCP/445 are commonly associated with Windows networking and remote/file-sharing functionality. If such services are unnecessarily exposed, they can increase the attack surface.

TCP/5432 is commonly used by PostgreSQL. Database services should generally be restricted to trusted hosts and should not be unnecessarily exposed to untrusted networks.

TCP/9080 returned an HTTP 301 response during service detection, but Nmap could not reliably identify the underlying application. Further application-level investigation would be required before making security conclusions.

## 10.0.2.3

TCP/53 was detected as open. Nmap reported the service as `tcpwrapped`, so the exact DNS implementation could not be determined.

### Security considerations

DNS services should be appropriately restricted and configured. Unnecessary exposure of network services can increase the attack surface.

## Important observation

An open port does not automatically mean that the service is vulnerable. It indicates that a service is listening and reachable. Further assessment would be required to determine whether a vulnerability actually exists.
