


# 📊 ELK Stack Setup Guide

This project provides step-by-step instructions to set up an **ELK Stack (Elasticsearch, Logstash, Kibana)** with agents like **Filebeat, Winlogbeat, Metricbeat, Auditbeat, and Packetbeat** for centralized logging and monitoring.

---

## 🚀 Architecture

`+--------------------+       +-------------------+ | Windows 10 Agent   | --->  |                   | | Winlogbeat         |       |                   | +--------------------+       |                   |                              |    ELK Server      | +--------------------+       |  (Ubuntu 22.04)    | | Kali Linux Agent   | --->  |                   | | Filebeat / Auditd  |       |                   | +--------------------+       +-------------------+                                    |    |                                    |    +--> Kibana (Web GUI)                                    |                               Elasticsearch (Storage)                                    |                                Logstash (Parsing)`

---

## 🧱 Components

- **Elasticsearch** → Stores logs and data
    
- **Logstash** → Parses and processes logs
    
- **Kibana** → Web dashboard for visualization
    
- **Beats (Agents)** → Send logs from endpoints
    
    - _Filebeat_ → Log files
        
    - _Winlogbeat_ → Windows event logs
        
    - _Auditbeat_ → Security/audit events
        
    - _Metricbeat_ → System metrics
        
    - _Packetbeat_ → Network traffic
        

---

## ⚡ Prerequisites

- Ubuntu 22.04 for ELK Server
    
- Windows 10 (Winlogbeat Agent)
    
- Kali Linux (Filebeat/Auditbeat Agent)
    
- Basic Linux/Windows admin knowledge
    

---

## 🔧 Installation

- ELK Server Setup
    
- Kali Linux Agent Setup
    
- Windows 10 Agent Setup
    
- Optional Beats Setup
    

👉 Each step is documented with configuration files and service commands.

---

## 🌐 Access Kibana

Once setup is complete, visit:

`http://<elk-server-ip>:5601`

---

## 🛠️ Useful Commands

`# Check service status 
```
sudo systemctl status elasticsearch 
sudo systemctl status kibana 
sudo systemctl status logstash 
```

# Test Beats config sudo filebeat test config sudo metricbeat test config`

---

## 📌 Next Steps

- Add more Beats for richer monitoring
    
- Secure ELK with TLS + authentication
    
- Create custom Kibana dashboards
    

---

## 📷 Screenshots (Optional)

You can add screenshots like:

`![Kibana Dashboard](images/kibana-dashboard.png)`

---

## 📜 License

MIT License