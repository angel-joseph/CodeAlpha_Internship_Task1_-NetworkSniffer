# CodeAlpha_Internship_Task1_-NetworkSniffer
This Python script is a simple packet sniffer built using the Scapy library. It captures TCP packets from a specified network interface and logs the details of each TCP connection to a file. The script defines a `handle_packet` function that processes each packet, extracting the source and destination IP addresses and ports from the TCP layer, and writes this information to a log file. The `main` function sets up the sniffer, specifying the network interface (`wlan0`) to listen on and whether to run in verbose mode, which provides additional output for debugging purposes. The script is designed to be run from the command line, accepting the network interface name as a mandatory argument and an optional "verbose" argument to enable verbose mode. The `sniff` function from Scapy is used to capture packets, invoking `handle_packet` for each packet. Proper exception handling ensures that the script can be gracefully terminated using a keyboard interrupt (Ctrl+C). The log file is named based on the network interface, ensuring clarity in the log data captured.
### Network Sniffer and Its Uses

A network sniffer, also known as a packet sniffer, is a tool used for monitoring and analyzing network traffic. It captures data packets traveling over a network and can provide detailed information about the network's activity. Network sniffers can be implemented in software or hardware, and they are commonly used by network administrators, security professionals, and developers. Here’s an overview of its uses:

1. **Network Monitoring and Troubleshooting:**
   - **Diagnosing Network Problems:** Network sniffers help identify network issues such as slow performance, bottlenecks, and connectivity problems by analyzing traffic patterns and pinpointing problematic areas.
   - **Bandwidth Utilization:** They monitor bandwidth usage to detect excessive consumption by certain devices or applications, helping in optimizing network performance.

2. **Security Analysis:**
   - **Intrusion Detection:** Sniffers can detect suspicious activities and potential security breaches by monitoring for unusual traffic patterns, unauthorized access attempts, and known attack signatures.
   - **Network Forensics:** In the event of a security incident, sniffers provide detailed packet-level data, aiding in the investigation and reconstruction of the incident.

3. **Protocol Analysis:**
   - **Protocol Debugging:** Developers use sniffers to analyze the behavior of network protocols, ensuring they function correctly and efficiently. This is crucial for debugging and improving networked applications.
   - **Protocol Compliance:** Ensuring that network devices and software comply with standard protocols and communicate correctly.

4. **Performance Analysis:**
   - **Application Performance:** By analyzing the traffic between applications and their servers, sniffers can identify performance issues and latency problems.
   - **Quality of Service (QoS):** Sniffers help in monitoring QoS parameters to ensure that critical applications receive the necessary bandwidth and performance levels.

5. **Data Collection for Reporting and Auditing:**
   - **Network Usage Reports:** Regular monitoring and logging of network traffic can generate reports on usage patterns, which are useful for capacity planning and resource allocation.
   - **Compliance Audits:** Organizations may use sniffers to ensure compliance with regulatory requirements by monitoring and logging network activity.

### How a Network Sniffer Works

A network sniffer captures data packets as they travel over a network. Here’s a simplified explanation of its working process:

1. **Packet Capture:** The sniffer listens to the network interface card (NIC) in promiscuous mode, capturing all packets, regardless of their destination.
2. **Packet Decoding:** The captured packets are decoded to extract information such as source and destination IP addresses, port numbers, protocol types, and payload data.
3. **Packet Analysis:** The decoded data is analyzed to identify patterns, anomalies, and specific details of interest, such as the type of protocol used or the presence of certain flags in the packet headers.
4. **Logging and Reporting:** The relevant information is logged for further analysis, reporting, or real-time monitoring.

### Popular Network Sniffers

- **Wireshark:** One of the most popular and powerful network protocol analyzers, widely used for troubleshooting, analysis, and education.
- **tcpdump:** A command-line packet analyzer that provides a detailed view of network traffic, often used in Unix-like operating systems.
- **Snort:** An open-source network intrusion detection system (NIDS) that also has packet sniffing capabilities.

Network sniffers are invaluable tools for managing and securing networks, providing insights that help maintain optimal performance, ensure security, and support compliance.
