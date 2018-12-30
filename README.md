```
[0 [12:32][leo@ansible]$ ansible all -i centos1, -m ping
centos1 | SUCCESS => {
    "changed": false, 
    "ping": "pong"
}
```

## How to supply arguments to the debug module:
```
ansible all -m debug --args msg=alv
```

## Pinging all the hosts using an asterisk
```
ansible '*' -m ping
```

## How to list all the hosts for a specific group:
```
ansible centos --list-hosts
```

```
[130 [12:57][leo@ansible]$ ansible '*' --list-hosts
  hosts (6):
    centos1
    centos2
    centos3
    ubuntu1
    ubuntu2
    ubuntu3
```

## How to use regexes to match hosts:
```
[centos]
centos1
centos2
centos3

[ubuntu]
ubuntu1
ubuntu2
ubuntu3
```

```
[0 [13:01][leo@ansible]$ ansible '~^.*3$' --list-hosts
  hosts (2):
    ubuntu3
    centos3
[0 [13:01][leo@ansible]$ 
```
