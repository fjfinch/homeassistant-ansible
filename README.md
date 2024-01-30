# <REPO NAME>
<REPO DESCRIPTION>

Change:
* README.md
* main.yml
* requirements.yml

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
git clone <REPO>
```

3 - Within `ansible/` - pull the required roles:
```bash
ansible-galaxy collection install -r requirements.yml
```

4 - Within `ansible/` - change the variables in `main.yml` & execute the playbook:
```bash
ansible-playbook main.yml -K
```
