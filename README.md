`
[0 [12:32][leo@ansible]$ ansible all -i centos1, -m ping
centos1 | SUCCESS => {
    "changed": false, 
    "ping": "pong"
}
`

## How to supply arguments to the debug module:
`
ansible all -m debug --args msg=alv
`