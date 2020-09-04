## ssh-key-switch
Switch ssh key pairs on the fly

### Motivation
If you work on a lot of projects in different hosting environments, there are potentially several ssh key pairs you need to manage for each of these environmennts.  Some cloud hosts, such as platform.sh, only allow you one ssh key pair regardless of the number of accounts you log in to use.  To make matters worse, you cannot use the key pair on different accounts.  This means you need a separate key pair for each account.  Switching between environments requires that the ssh private key change locally to access each account.  This script helps make it easier to perform this switch.

### Installation
```bash
$ git clone git@github.com:uberhacker/ssh-key-switch.git
$ sudo cp ssh-key-switch/ssh-key-switch /usr/local/bin/
```

### Usage
```bash
$ ssh-key-switch <name>
```
Copy all the keys you want to switch in `~/.ssh` with the `<name>` prefix.

### Example
```bash
$ cd ~/.ssh
$ cp id_rsa <name>.id_rsa
$ cp id_rsa.pub <name>.id_rsa.pub
```
If `<name>` is `local`, then to switch keys, type `ssh-key-switch local`.

This will copy all the keys named `local.id_rsa*` to `id_rsa*`.
