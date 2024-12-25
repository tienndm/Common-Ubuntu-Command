# Firewall Configuration Commands on CentOS 7

## Checking Firewall Status
```bash
sudo firewall-cmd --state
```

## Starting and Stopping Firewall
```bash
sudo systemctl start firewalld
sudo systemctl stop firewalld
```

## Enabling and Disabling Firewall at Boot
```bash
sudo systemctl enable firewalld
sudo systemctl disable firewalld
```

## Reloading Firewall
```bash
sudo firewall-cmd --reload
```

## Listing All Firewall Rules
```bash
sudo firewall-cmd --list-all
```

## Adding a Service to the Firewall
```bash
sudo firewall-cmd --permanent --add-service=http
sudo firewall-cmd --permanent --add-service=https
sudo firewall-cmd --reload
```

## Removing a Service from the Firewall
```bash
sudo firewall-cmd --permanent --remove-service=http
sudo firewall-cmd --permanent --remove-service=https
sudo firewall-cmd --reload
```

## Adding a Port to the Firewall
```bash
sudo firewall-cmd --permanent --add-port=8080/tcp
sudo firewall-cmd --reload
```

## Removing a Port from the Firewall
```bash
sudo firewall-cmd --permanent --remove-port=8080/tcp
sudo firewall-cmd --reload
```

## Allowing Specific IP Address
```bash
sudo firewall-cmd --permanent --add-rich-rule='rule family="ipv4" source address="192.168.1.100" accept'
sudo firewall-cmd --reload
```

## Blocking Specific IP Address
```bash
sudo firewall-cmd --permanent --add-rich-rule='rule family="ipv4" source address="192.168.1.100" drop'
sudo firewall-cmd --reload
```

## Checking Active Zones
```bash
sudo firewall-cmd --get-active-zones
```

## Adding an Interface to a Zone
```bash
sudo firewall-cmd --zone=public --add-interface=eth0 --permanent
sudo firewall-cmd --reload
```

## Removing an Interface from a Zone
```bash
sudo firewall-cmd --zone=public --remove-interface=eth0 --permanent
sudo firewall-cmd --reload
```

## Listing Services in a Zone
```bash
sudo firewall-cmd --zone=public --list-services
```

## Adding a Service to a Zone
```bash
sudo firewall-cmd --zone=public --add-service=ssh --permanent
sudo firewall-cmd --reload
```

## Removing a Service from a Zone
```bash
sudo firewall-cmd --zone=public --remove-service=ssh --permanent
sudo firewall-cmd --reload
```

## Checking Firewall Configuration
```bash
sudo firewall-cmd --list-all
```