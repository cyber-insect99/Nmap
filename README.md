
![Logo](https://github.com/cyber-insect99/photo-gallery-/blob/main/nmap.png?raw=true)

##   Fundamental

- Scanning remote hosts and listing open ports 
- Identifying services of a remote host
- Identifying services of a remote hosts
- Scanning using specific port ranges
-  Identifying live hosts in local networks
- Specifying network interface for scanning
- NSE scripts


## Scanning remote hosts and listing open ports 



```bash
  
• Ping scanme.nmap.org (reachability is mandatory)
• nmap scanme.nmap.org
• nmap –v scanme.nmap.org (what happening in background)
• nmap –v –dns-servers 1.1.1.1 scanme.nmap.org (how scan happening –v)
• nmap –v –dns-servers 1.1.1.1, 4.4.4.4 scanme.nmap.org
• nmap –n scanme.nmap.org (reverse dns resolution)
• nmap –p1-30 scanme.nmap.org
• nmap –p4444 scanme.nmap.org
• nmap –p81 scanme.nmap.org
• nmap –p443 scanme.nmap.org
• nmap –dns-servers 1.1.1.1 –p443 scanme.nmap.org
```

## Identifying services of a remote hosts

Service Version Detection


```bash 
• nmap –sV –v scanme.nmap.org
• nmap –sV –version-intensity 9 scanme.nmap.org
• nmap –A scanme.nmap.org (Aggressive Detection)
• nmap –sC –sV 0 scanme.nmap.org –v (-A and this is identical, same info will show)
```

## Identifying services of a remote hosts

Finding live host in a local area networks


```bash
• netdiscover (show all live host)
• nmap –sP –send-ip 192.168.0.1/24
• nmap –sP –script discovery 192.168.7.1/24
```


## Fundamental

Scanning using specific port ranges


```bash
• nmap –p80 google.com -v
• nmap –p443 google.com –v
• nmap –p4444 google.com –v
• nmap –p81 google.com –v
• nmap –p80 192.168.0.1/24 –v (for local network)
• nmap –p80 localhost –v
• nmap –p80 127.0.0.1 –v (localhost=127.0.0.1)
• nmap –p80,443,2000,2000,4444 google.com (scan multiple port status of a web-site)
• nmap –p1-100 google.com (scan port range status of google.com)
• nmap –p- google.com (scan all ports of google. Mostly this command use for local network)
• Nmap –p http localhost
• Nmap –p http” localhost (result you going to get is everything related to this service)
• Nmap –p https” cyberbangla.org
• Nmap –p[1-65535] scanme.nmap.org (scan 1 to 65535 port)
• Nmap –p[1-65535] localhost (only scan for localhost)
• Nmap –p[1-65535] 192.168.7.1/24 –v (scanning localhost and scan all ports)
```




Finding live host in a local area networks


```bash
• netdiscover (show all live host)
• nmap –sP –send-ip 192.168.0.1/24
• nmap –sP –script discovery 192.168.7.1/24
```



## NSE Script

Finding live host in a local area networks



```bash
• nmap –sV –script http-title scanme.nmap.org
• nmap –sV –script http-title, http-headers scanme.nmap.org (can add another script)
• nmap–script vuln scanme.nmap.org –v (run all the scripts)
```


## Gathering Information

Finding live host in a local area networks



```bash
• nmap –sV –script http-title scanme.nmap.org
• nmap –sV –script http-title, http-headers scanme.nmap.org (can add another script)
• nmap–script vuln scanme.nmap.org –v (run all the scripts)
```



## OS Identification



```bash
• nmap –O nmap.scanme.org –v
• nmap –O –max-os-tries=1 scanme.nmap.org
• Tcp.port==135
```




## UDP Service

```bash
• nmap –sU -p- scanme.nmap.org
• nmap -sU -F scanme.nmap.org –v
• nmap –F –p1-400 –sU scanme.nmap.org -v
```


## Identifying protocols on remote hosts

```bash
• nmap –sO scanme.nmap.org
• nmap –sO localhost
• nmap –sO –v 192.168.0.1/24
```


##  Discovering and Identifying Firewall Identifying protocols on remote hosts

```bash
• nmap –sA 192.168.43.69
• nmap –p80 –sA 192.168.43.69 –v
• nmap –p1-100 –sA 192.168.43.204 –v
• nmap -p- -sA 192.168.43.204 –v
```


##  Identifying services with vulnerabilities

```bash
• nmap –sA 192.168.43.69
• nmap –p80 –sA 192.168.43.69 –v
• nmap –p1-100 –sA 192.168.43.204 –v
• nmap -p- -sA 192.168.43.204 –v
```


##  Using zombie hosts to spoof origin of ports scans


```bash
• nmap –sA 192.168.43.69
• nmap –p80 –sA 192.168.43.69 –v
• nmap –p1-100 –sA 192.168.43.204 –v
• nmap -p- -sA 192.168.43.204 –v
```

All credits goes to @cyber bangal

  ![Logo](https://cdn.icon-icons.com/icons2/2148/PNG/512/nmap_icon_132152.png   )
