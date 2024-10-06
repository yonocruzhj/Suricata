<h1>Suricata: Examining Alerts, Logs, and Rules</h1>

<h2>Description</h2>
This project demonstrates how to use Suricata, an open-source network threat detection engine, to monitor network traffic and analyze output logs for security insights. This repository includes setup instructions, configuration files, and example scripts to parse and visualize Suricata logs.

<br />

<h2> Utilities</h2>

- <b>Suricata</b>
- <b>jq (for JSON manipulation)</b> 

<h2>Environments </h2>

- <b>Kali Linux</b> 

<h2>Walk-through:</h2>

<p align="center">
Scenario: <br/>
<img src="https://imgur.com/5Rbl9vG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Custom Rule  <br/>
<img src="https://imgur.com/IR4JS7Q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
The first line in the screenshot above is the code I ran to display the custom rule given. The output suggests this signature triggers an alert when Suricata observes the text 'GET' as the HTTP method in an HTTP packet from the internal network going to the external environment.

<br />
<h2>Running suricata using the custom rule</h2> <br/>
<img src="https://imgur.com/AIDnBfE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
In the above screenshot, the input initiates the Suricata application and processes the sample.pcap file using the rules in the custom.rules file. The output states how many packets were processed.

<br />
<h2>Triggering the alert and examining the output logs in the 'fast.logs' file: </h2> 
<br/>
<img src="https://imgur.com/vGA9nve.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
The screenshot shows details of the alerts in the fast.logs file such as the timestamps, signature alert, protocol, source IP address, and destination IP address.
<br />
<h2>Output of eve.json file :</h2>  <br/>
<img src="https://imgur.com/HxK7rT5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br /> 
The above output is the details of the first alert in the eve.json file. One item I was asked to find was the severity level, which is 3 as indicated in the screenshot.
<br />
<h2>Specific details in eve.json file</h2>  <br/>
<img src="https://imgur.com/1KU4JuE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
The input of the above screenshot extracted all the details that I requested and excluded any additional information. The fields selected are the timestamp (.timestamp), the flow id (.flow_id), the alert signature or msg (.alert.signature), the protocol (.proto), and the destination IP address (.dest_ip).
<br />

<h2>Summary</h2>

This project increased my familiarity with Suricata, triggering alerts, examining alert signatures, and examining components of output logs.


