# IWAN Lab Setup with Ansible

This repository shows how to apply a basic DMVPN hub configuration on an ISR router using Ansible.

## Features

- Deploys a `Tunnel0` interface with DMVPN configurations.
- Uses standard Ansible `ios_config` module.
- Easily customizable in `roles/dmvpn_hub/vars/main.yml`.

## Prerequisites

- Ansible installed on your control machine.
- Access to a Cisco ISR router (virtual or physical) for the lab.
- Basic understanding of DMVPN and IWAN concepts.

## How to Run

1. Update `inventory.yml` with the ISR device details.
2. Customize variables in `roles/dmvpn_hub/vars/main.yml` if needed.
3. `ansible-playbook -i inventory.yml playbook.yml`
4. Verify DMVPN configuration on the router (`show dmvpn`, `show ip nhrp`).
