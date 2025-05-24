Ansible-LAMP
Ansible-LAMP is an automation project designed to deploy a full LAMP (Linux, Apache, MySQL, PHP) stack using Ansible. This setup streamlines the provisioning of web servers for development or production environments.

Features
Automated Deployment: Leverages Ansible playbooks to install and configure Apache, MySQL, and PHP seamlessly.

Modular Structure: Utilizes Ansible roles for organized and reusable configurations.

Environment Management: Supports multiple environments through inventory files.

Customizable Variables: Defines configurable parameters in group_vars for flexibility.

Project Structure
bash
Copy
Edit
Ansible-Lamp/
├── group_vars/
│   └── all.yml             # Global variables for all hosts
├── inventories/
│   └── hosts               # Inventory file defining target servers
├── roles/
│   ├── apache/             # Role for Apache installation and configuration
│   ├── mysql/              # Role for MySQL installation and configuration
│   └── php/                # Role for PHP installation and configuration
└── site.yml                # Main playbook to orchestrate the roles
Prerequisites
Ansible: Ensure Ansible is installed on your control node.

Target Servers: Remote servers should be accessible via SSH and have Python installed.

Usage
Clone the Repository:

bash
Copy
Edit
git clone https://github.com/kasun-kalhara/Ansible-Lamp.git
cd Ansible-Lamp
Configure Inventory:
Edit the inventories/hosts file to specify your target servers.

Customize Variables:
Modify group_vars/all.yml to set variables like MySQL root password, PHP versions, etc.

Run the Playbook:

bash
Copy
Edit
ansible-playbook -i inventories/hosts site.yml
