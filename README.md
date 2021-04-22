# agoric-os-metrics-dashboard

----
---

## How To Setup ?

---

### 1. Setup Prometheus
Step1: Get tar.gz file
```
wget https://github.com/prometheus/prometheus/releases/download/v2.11.1/prometheus-2.11.1.linux-amd64.tar.gz
```
Step2: Extract The Tar
```
tar -xvzf prometheus-2.11.1.linux-amd64.tar.gz
```
Step3: Move into that Directory
```
cd prometheus-2.11.1.linux-amd64
screen
```
Step 4: Execute The Binary File Using The Below Command:
```shell
./prometheus
```
Step 5: Get out of that screen
```shell
Press control+A+D
```
### 2. Setup Node Exporter in a Different Screen Similarly
```shell
wget https://github.com/prometheus/node_exporter/releases/download/v0.18.1/node_exporter-0.18.1.linux-amd64.tar.gz
tar -xvzf node_exporter-0.18.1.linux-amd64.tar.gz
mv node_exporter-0.18.1.linux-amd64 node_exporter
cd node_exporter
./node_exporter
```

### 3. Setup Grafana in a Different Screen Similarly
```shell
wget https://dl.grafana.com/oss/release/grafana-6.4.4.linux-amd64.tar.gz
tar xvf grafana-6.4.4.linux-amd64.tar.gz
cd grafana-6.4.4/
./grafana-server
```

### 4. Add Node Exporter in Prometheus config
```shell
 static_configs:
      - targets: ['localhost:9100']
```
### 5. Open Grafana and import the dashboard by json provided in the repo

1. [System Overview](/dashboards/SystemOverview.json)
2. [Compare System Parameters](/dashboards/CompareSystemParameters.json)
3. [CpuUtilization Details](/dashboards/CpuUtilizationDetails.json)
4. [Disk Space](/dashboards/DiskSpace.json)
5. [Network Overview](/dashboards/NetworkOverview.json)

## Snapshots

----

### Landing Page
![](snapshots/HomeDashboard.png)
### 1. System Overview
![](snapshots/SystemOverview.png)
### 2. Compare System Parameters
![](snapshots/CompareSystemParameters.png)
### 3. Cpu Utilization Details
![](snapshots/CpuUtilizationDetails.png)
### 4. Disk Space
![](snapshots/DiskSpace.png)
### 5. Network Overview
![](snapshots/NetworkOverview.png)

----
Made By KingSuper
