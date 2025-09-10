# Introductory Networking
  * Room: Introductory Networking<br>
  * Difficulty: Easy<br>
  * Category: Network<br>
  * Date Completed: 15-08-2025<br>
  * Link: https://tryhackme.com/room/introtonetworking

# Purpose 
  * I’ve learned networking before, but this room was suggested in a Medium article, so I decided to try it too.<br>
  Here's the link to the article : https://medium.com/@polygonben/ejpt-a-guide-on-how-to-pass-first-time-f8cec3f79a73<br>

# Key Learnings 
  * Learned about OSI and TCP/IP Models, Process of encapsulation and De-encapsulation, How three-way handshake works,
  and also learned about some basic tools like : ping, traceroute, WHOIS, Dig.<br>

# Tools 
  * ping : The ping command is used when we want to test whether a connection to a remote resource is possible.<br>
  
```bash
shaivarth@Sarthaks-MacBook-Air-4 ~ % ping google.com
PING google.com (142.251.220.46): 56 data bytes
64 bytes from 142.251.220.46: icmp_seq=0 ttl=111 time=376.303 ms
64 bytes from 142.251.220.46: icmp_seq=1 ttl=111 time=73.806 ms
64 bytes from 142.251.220.46: icmp_seq=2 ttl=111 time=72.436 ms
64 bytes from 142.251.220.46: icmp_seq=3 ttl=111 time=88.115 ms
64 bytes from 142.251.220.46: icmp_seq=4 ttl=111 time=317.995 ms
64 bytes from 142.251.220.46: icmp_seq=5 ttl=111 time=186.768 ms
64 bytes from 142.251.220.46: icmp_seq=6 ttl=111 time=77.118 ms
64 bytes from 142.251.220.46: icmp_seq=7 ttl=111 time=83.780 ms
64 bytes from 142.251.220.46: icmp_seq=8 ttl=111 time=56.956 ms
```
  * traceroute : Traceroute can be used to map the path your request takes as it heads to the target.<br>


```bash
shaivarth@Sarthaks-MacBook-Air-4 ~ % traceroute google.com
traceroute to google.com (142.251.42.238), 64 hops max, 40 byte packets
 1  172.25.160.1 (172.25.160.1)  7.003 ms  5.422 ms  5.004 ms
 2  172.25.90.2 (172.25.90.2)  6.567 ms  8.570 ms  14.963 ms
 3  139.167.143.181 (139.167.143.181)  12.206 ms  8.195 ms  19.161 ms
 4  * * *
 5  * 172.26.40.7 (172.26.40.7)  30.591 ms
    172.16.92.145 (172.16.92.145)  34.276 ms
 6  172.16.92.145 (172.16.92.145)  50.320 ms
    172.26.40.7 (172.26.40.7)  30.083 ms *
 7  173.194.121.8 (173.194.121.8)  344.692 ms * *
 8  142.250.208.148 (142.250.208.148)  1009.191 ms
    142.250.214.109 (142.250.214.109)  30.352 ms
    142.250.238.80 (142.250.238.80)  27.547 ms
 9  192.178.110.206 (192.178.110.206)  33.309 ms
    142.250.214.107 (142.250.214.107)  25.482 ms
    192.178.86.238 (192.178.86.238)  30.909 ms
10  tsa01s11-in-f14.1e100.net (142.251.42.238)  29.455 ms  26.388 ms  36.980 ms
```
  * whois : Whois essentially allows you to query who a domain name is registered to, you can potentially get a great deal of information from a whois search. Sometimes some data is Redacted, like i searched for my college website   [vitbhopal.ac.in], most info was 'REDACTED'.

```bash
shaivarth@Sarthaks-MacBook-Air-4 ~ % whois google.com
% IANA WHOIS server
% for more information on IANA, visit http://www.iana.org
% This query returned 1 object

refer:        whois.verisign-grs.com

domain:       COM

organisation: VeriSign Global Registry Services
address:      12061 Bluemont Way
address:      Reston VA 20190
address:      United States of America (the)

contact:      administrative
name:         Registry Customer Service
organisation: VeriSign Global Registry Services
address:      12061 Bluemont Way
address:      Reston VA 20190
address:      United States of America (the)
phone:        +1 703 925-6999
fax-no:       +1 703 948 3978
e-mail:       info@verisign-grs.com

contact:      technical
name:         Registry Customer Service
organisation: VeriSign Global Registry Services
address:      12061 Bluemont Way
address:      Reston VA 20190
address:      United States of America (the)
phone:        +1 703 925-6999
fax-no:       +1 703 948 3978
e-mail:       info@verisign-grs.com
```
When searched for my college website:
```bash

shaivarth@Sarthaks-MacBook-Air-4 ~ % whois vitbhopal.ac.in
% IANA WHOIS server
% for more information on IANA, visit http://www.iana.org
% This query returned 1 object
Domain Name: vitbhopal.ac.in
Registry Domain ID: D414400000000585585-IN
Registrar URL: http://www.ernet.in
Updated Date: 2017-08-18T04:53:00.925Z
Creation Date: 2016-04-01T06:19:57.482Z
Registry Expiry Date: 2027-04-01T06:19:57.482Z
Registrar: ERNET India
Registrar IANA ID: 800068
Registrar Abuse Contact Email: tejalt@eis.ernet.in
Registrar Abuse Contact Phone: +91.1123358248
Domain Status: ok https://icann.org/epp#ok
Registry Registrant ID: REDACTED FOR PRIVACY
Registrant Name: REDACTED FOR PRIVACY
Registrant Organization: VIT University
Registrant Street: REDACTED FOR PRIVACY
Registrant City: REDACTED FOR PRIVACY
Registrant State/Province: 
Registrant Postal Code: REDACTED FOR PRIVACY
Registrant Country: IN
Registrant Phone: REDACTED FOR PRIVACY
Registrant Fax: REDACTED FOR PRIVACY
Registrant Email: Please query the RDDS service of the Registrar of Record identified in this output for information on how to contact the Registrant, Admin, or Tech contact of the queried domain name.
Registry Admin ID: REDACTED FOR PRIVACY
Admin Name: REDACTED FOR PRIVACY
Admin Organization: REDACTED FOR PRIVACY
Admin Street: REDACTED FOR PRIVACY
Admin City: REDACTED FOR PRIVACY
Admin State/Province: REDACTED FOR PRIVACY
Admin Postal Code: REDACTED FOR PRIVACY
Admin Country: REDACTED FOR PRIVACY
Admin Phone: REDACTED FOR PRIVACY
Admin Fax: REDACTED FOR PRIVACY

```                                                            
# Lessons Learned

 1. The ping command can be used to test reachability and latency.
 2. TTL (Time To Live) values indicate network hops allowed.
 3. traceroute shows intermediate hops between the source and destination.
 4. '*' indicates packet loss or filtered ICMP responses.
 5. High latency in some hops may indicate network congestion.
