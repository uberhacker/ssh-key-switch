## ssh-key-switch
Switch ssh key pairs on the fly

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
