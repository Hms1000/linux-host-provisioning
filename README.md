# Linux Host Provisioning
An Ansible project demonstrating how I automate the provisioning and hardening of a fresh Ubuntu server.

## Features

This playbook performs the following tasks:

- Sets the system hostname
- Updates the APT package cache
- Enables and configures SSH
- Disables SSH root login
- Disables SSH password authentication
- Configures UFW firewall rules
- Creates local users
- Deploys Netplan network configuration
- Installs common administration packages
- Installs and enables Fail2ban

### Prerequisites

Before running the playbook, ensure the following requirements are met:

- Ubuntu Server
- Bash shell environment
- Ansible installed on the control node
- SSH access to the target host
- Sudo privileges on the target host

#### Installation

Clone the repository:

```bash
git clone git@github.com:Hms1000/linux-host-provisioning.git
cd linux-host-provisioning
```

##### Project Structure
```text
linux-host-provisioning/
├── ansible.cfg
├── inventory
├── baseline.yml
└── README.md
```

###### Usage

Update the inventory file with your target hosts:

```ini
[ubuntu]
192.168.1.100
```

Run the playbook:
```bash
ansible-playbook -i inventory baseline.yml
```