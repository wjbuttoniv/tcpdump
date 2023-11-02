# Analyzing Network Traffic for Potential Intruders

This project aims to showcase the process of capturing and analyzing network traffic to detect potential intruders within our network. \

In this project, we will simulate a scenario where an unauthorized user attempts to gain access to our network. Our goal is to capture and analyze their network traffic. To do this, we will use SSH on our local machine to create a controlled environment for our simulation.


### Step 1: Preparing the tcpdump Statement

![prepstatement](https://github.com/wjbuttoniv/tcpdump/blob/main/tcpdump/Pasted%20image%2020231101111942.png?raw=true)

We start by preparing a tcpdump command to capture network traffic. This command will monitor a specific port, and we will save the captured data to a file for analysis. Here's a breakdown of the command:

    sudo tcpdump: This runs tcpdump as a superuser, ensuring access to all necessary network data.
    port 22: Defines the target port for traffic monitoring, in this case, port 22 which is commonly used for SSH.
    -i: Specifies the network interface to capture data from, set as "any" to monitor all available interfaces.
    -w: Instructs tcpdump to write its output to a file, named "proof.pcap" in this case.
    -G: Defines the duration of traffic capture, set to 600 seconds (10 minutes) in this example.
    -C: Specifies the maximum file size before creating a new file, set as 2MB.

### Step 2: Simulating the Attack

To create a comprehensive packet capture, we run the simulation multiple times. This allows us to gather a more complete set of data to analyze.

![thebackdoor](https://github.com/wjbuttoniv/tcpdump/blob/main/tcpdump/Pasted%20image%2020231101112331.png?raw=true)

### Step 3: Analyzing the Captured Data

Once the data is captured, we can analyze it to determine if someone attempted to breach our network. To make this process more manageable, we will open the captured data in Wireshark, a network protocol analyzer that makes it easier to interpret the traffic.

![tcpdumpread](https://github.com/wjbuttoniv/tcpdump/blob/main/tcpdump/Pasted%20image%2020231101112549.png?raw=true)

![wireshark](https://github.com/wjbuttoniv/tcpdump/blob/main/tcpdump/Pasted%20image%2020231101112855.png?raw=true)

In a real-world scenario involving an external attack, the host IP address recorded in the captured traffic would likely be different from our own. By capturing and analyzing this data, we can investigate whether someone tried to engage in malicious activities within our network.

### Summary

This project demonstrates the process of capturing and analyzing network traffic to identify potential intruders within our network. By simulating an attack and using tools like tcpdump and Wireshark, we can detect suspicious activity and take necessary actions to enhance network security.
