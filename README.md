# casper-node-setup

## Follwing official guide and pay attention on below note

---

### Add Casper repository
Becarefull don't run this command twice
``` shell
echo "deb https://repo.casperlabs.io/releases" bionic main | sudo tee -a /etc/apt/sources.list.d/casper.list
```

if getting this warnning after run `sudo apt update`
``` shell
N: Skipping acquire of configured file 'main/binary-i386/Packages' as repository 'https://repo.casperlabs.io/releases bionic InRelease' doesn't support architecture 'i386'
```

Check if repo already added by running. We only need one line of repo
``` shell
sudo nano /etc/apt/sources.list.d/casper.list
```

---

### Install pre-requisites for building smart contracts


Run this after install Rustup
``` shell
source $HOME/.cargo/env
```

---
### Server Migration

Can the user try to compress the file with:
```
tar -cSjf <archive>.tar.bz2 /path/to/sparse/file
```
Then transfer the archive with scp, and extract it as normal on the target path:
```
tar -xvf <archive>.tar.bz2 
```
I suggest to try with the single files rather than the whole directory