# Ansible: Postleaf CMS Playbook

Ansible playbook to install and run Postleaf CMS on Ubuntu/Debian servers.

## Version

Postleaf: 1.0.0-alpha.3

## Usage

__NOTE:__ The following instructions are for Ubuntu 16.04


### Install Ansible:

1. First add the Ansible PPA (after which you'll need to press ENTER to confirm): `sudo apt-add-repository ppa:ansible/ansible`
2. Update system's package index: `sudo apt-get update`
3. Install Ansible: `sudo apt-get install -y ansible`

### Clone repository

1. Install git: `sudo apt-get install -y git`
2. Change into home directory: `cd ~`
3. Clone repo: `git clone https://github.com/lukewatts/postleaf-playbook.git`

### Run

1. Change directory into repo: `cd ~/postleaf-playbook`
2. Set your `app_url` variable in site.yml under vars to your ip or domain (no trialing slash): `app_url: https://example.com`
2. Run playbook: `ansible-playbook site.yml`

### Troubleshooting

If you experience issues with CSS not loading correctly please verify the `app_url` var in `site.yml` is correct. No trailing slash and include the protocol.

__CORRECT:__ `http://127.0.0.1` or `https://example.com` 
__INCORRECT:__ `localhost` or `http://127.0.0.1/`

## Licence

MIT

&copy; 2017 Luke Watts




