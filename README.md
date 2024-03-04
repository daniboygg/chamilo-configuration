# Utility to install chamilo using docker and ansible

Install ansible dependencies:

```bash
ansible-galaxy install -r ansible/requirements.yml
```

Install all needed packages and configure chamilo

```bash 
ansible-playbook ansible/setup.yml --ask-become-pass
```

You can modify the following variables to change paths according to your needs:
* chamilo_dir: path were chamilo was cloned from git
* apache_alias: which url apache should accept in addition to localhost

Start database in a docker container: 

```bash 
docker compose up --build
```

Review instructions in https://github.com/chamilo/chamilo-lms to install chamilo-lms (this project only configure
its dependencies)
You can start chamilo configuration visiting http://localhost