# homeassistant-ansible
Ansible playbook for deploying and configuring a Home Assistant container

## Install & setup
To use this repo, a couple of tools are required:

* git (to clone the repo)
* pipx (to install ansible)
* ansible (to configure the system)

1 - Oneliner to install all above:
```bash
sudo apt update && sudo apt install -y git pipx && pipx install ansible --include-deps && . ~/.profile
```

2 - Clone this repository:
```bash
git clone https://github.com/fjfinch/homeassistant-ansible.git
```

3 - Pull the required roles:
```bash
ansible-galaxy collection install -r requirements.yml
```

4 - Execute the playbook:
> Note: for a stock installation without any custom configs, remove `tasks/3_personal.yml` from `main.yml`
```bash
ansible-playbook main.yml -K
```

---

Todo:
```
<USER> -> Advanced mode -> on
<USER> -> Time format -> use system locale
<USER> -> Number format -> use system locale
Settings -> Devices & services -> Sun -> *x* entities -> enable sun_solar_rising

Remove Map dashboard
Remove unused integrations
Add integrations
Change names zigbee devices
Add helpers
Add phone companion app
```
