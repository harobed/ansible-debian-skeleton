```
$ pipenv install
$ pipenv shell
```

```
$ vagrant up
```

```
$ ansible -m ping all
my_server | SUCCESS => {
    "changed": false,
    "ping": "pong"
}
```

```
$ ansible-playbook playbooks/install-base.yml
```
