# ansible-imapfilter-gmail_clean

ansible-imapfilter-gmail_clean is an Ansible role to install and configure imapfilter on a debian based OS to clean gmail trash and spam folders.

It performs: 

* installation of imapfilter package
* creation of dedicated user and group for imapfilter runs
* creation of dedicated folder for imapfilter configurations and logs
* configuration of gmail account to be cleaned
* installation, start and enable of a dedicated systemd unit

## Install
### Clone
```bash
git clone https://github.com/lgaggini/ansible-imapfilter-gmail_clean.git
```
## Configuration

The configuration is done by vars listed and explained in [defaults/main.yml](https://github.com/lgaggini/ansible-imapfilter-gmail_clean/blob/master/defaults/main.yml) file.

## Usage

```
- name: bootstrap an ubuntu cloud image for imapfilter
  hosts: imapfiltterserver
  vars_files:
    - group_vars/imapfilter.yml

  roles:
    - { role: imapfilter, tags: ['imapfilter'] }
```

## Credits
[Automatic Gmail’s Trash & Spam folders cleanup](https://www.dragonsreach.it/2011/07/03/automatic-gmails-trash-spam-folders-cleanup/)
