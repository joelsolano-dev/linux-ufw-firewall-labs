# Linux UFW Firewall Hardening & Configuration

Practical lab documenting the step-by-step deployment of an Uncomplicated Firewall (UFW) baseline on a Linux environment.

---

## Objective
Protect a Linux production instance by dropping all unsolicited inbound traffic, allowing necessary administrative access (SSH), and opening essential web services.

## Configuration Steps

### 1. Default Policy Baseline
Set strict perimeter boundaries by blocking all incoming traffic and allowing outgoing connections:
```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow 22/tcp
sudo ufw allow 80/tcp
sudo ufw allow 443/tcp
sudo ufw enable
sudo ufw status verbose
