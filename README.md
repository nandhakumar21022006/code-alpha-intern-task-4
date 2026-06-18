# code-alpha-intern-task-4

# 🔒 Cyber Security Internship – Task 4

# Network Intrusion Detection System using Snort

## 📌 Objective

The objective of this task was to set up and configure a Network Intrusion Detection System (NIDS) using Snort to monitor network traffic, detect suspicious activity, and generate alerts for potential threats.

## 🛠 Tools Used

* Kali Linux
* Snort 3
* ICMP (Ping) Traffic for Testing

## 🚀 Steps Performed

### 1. Installed and Verified Snort

Verified Snort installation using:

```bash
snort -V
```

### 2. Identified Network Interface

Used:

```bash
ip a
```

Interface detected:

```text
eth0
```

### 3. Started Network Monitoring

Executed:

```bash
sudo snort -i eth0 -A alert_fast
```

Snort successfully monitored live network traffic.

### 4. Generated Test Traffic

Used ping requests to generate network activity:

```bash
ping google.com
```

### 5. Created Custom Detection Rule

Configured a local rule to detect ICMP traffic:

```text
alert icmp any any -> any any (msg:"ICMP Ping Detected"; sid:1000001; rev:1;)
```

### 6. Alert Configuration

The custom rule was designed to generate alerts whenever ICMP packets were detected on the network.

## 🔍 Key Concepts Learned

* Network Intrusion Detection Systems (NIDS)
* Snort Architecture
* Network Traffic Monitoring
* Signature-Based Detection
* Custom Rule Creation
* Alert Generation

## 📊 Results

* Successfully deployed Snort IDS.
* Monitored network traffic in real time.
* Configured custom ICMP detection rules.
* Generated alerts for monitored traffic.

## ✅ Conclusion

This task provided hands-on experience with intrusion detection systems, network monitoring, and custom alert creation using Snort. It improved understanding of threat detection techniques and network security monitoring.
