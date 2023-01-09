# The solutions for known issues

## [Vagrant] DNS issue

- Issue

```bash
vagrant@vagrant:~$  git clone https://github.com/briansu2004/udemy-devops-9projects-free.git
Cloning into 'udemy-devops-9projects-free'...
fatal: unable to access 'https://github.com/briansu2004/udemy-devops-9projects-free.git/': Could not resolve host: github.com
```

- Solution

Run below commands to stop `systemd-resolved`

```bash
sudo systemctl disable systemd-resolved
sudo systemctl stop systemd-resolved
```

Add below entry to `/etc/resolv.conf`

```bash
nameserver 8.8.8.8 
nameserver 8.8.4.4
```


## [Vagrant] Port 53 error

- Issue

...

- Solution

Same as above `[Vagrant] DNS issue`

## ?