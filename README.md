# Utility to install chamilo using docker and ansible

Install ansible dependencies:

```bash
ansible-galaxy install -r ansible/requirements.yml
```

Install all needed packages and configure chamilo

```bash 
ansible-playbook ansible/setup.yml --ask-become-pass
```

Start database in a docker container: 

```bash 
docker compose up --build
```


You can start chamilo configuration visiting http://localhost