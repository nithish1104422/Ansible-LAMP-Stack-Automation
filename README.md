# Ansible LAMP Stack Deployment

This project automates the deployment of a LAMP stack (Linux, Apache, MySQL, PHP) on remote servers using Ansible.

## Features
- **Apache**: Deploys and configures the Apache HTTP server.
- **MySQL**: Installs MySQL, creates a database, and sets up user permissions.
- **PHP**: Configures PHP for dynamic content.

## Prerequisites
- Ansible installed on the control node.
- SSH access to the target servers.
- Inventory file configured with target server details.

## Setup
1. Clone this repository:
   ```bash
   git clone <your-repo-url>
   cd ansible-lamp-deployment

    Install required roles:

    ansible-galaxy install -r requirements.yml

    Update the inventory file: Edit inventories/dev/hosts to add your target server details.

Usage

Run the playbook to deploy the LAMP stack:

ansible-playbook -i inventories/dev/hosts site.yml

Directory Structure

ansible-lamp-deployment/
├── inventories/
│   ├── dev/
│   │   ├── group_vars/
│   │   │   ├── all.yml
│   │   │   └── lamp.yml
│   │   └── hosts
│   ├── staging/
│   │   ├── group_vars/
│   │   │   ├── all.yml
│   │   │   └── lamp.yml
│   │   └── hosts
├── roles/
│   ├── common/
│   │   ├── tasks/
│   │   │   └── main.yml
│   │   ├── handlers/
│   │   │   └── main.yml
│   │   ├── templates/
│   │   │   └── motd.j2
│   │   ├── files/
│   │   └── vars/
│   │       └── main.yml
│   ├── apache/
│   │   ├── tasks/
│   │   │   └── main.yml
│   │   ├── handlers/
│   │   │   └── main.yml
│   │   ├── templates/
│   │   │   └── httpd.conf.j2
│   │   └── vars/
│   │       └── main.yml
│   ├── mysql/
│   │   ├── tasks/
│   │   │   └── main.yml
│   │   ├── handlers/
│   │   │   └── main.yml
│   │   └── vars/
│   │       └── main.yml
│   ├── php/
│   │   ├── tasks/
│   │   │   └── main.yml
│   │   ├── templates/
│   │   │   └── php.ini.j2
│   │   └── vars/
│   │       └── main.yml
├── site.yml
├── requirements.yml
└── README.md

License

This project is licensed under the MIT License.


---

### Steps to Use:
1. Place these files in the root of your project directory.
2. Run the playbook as documented in the README.


