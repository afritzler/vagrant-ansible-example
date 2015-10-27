# vagrant-ansible-example
Sample Vagrant project to use the Ansible provisioner. It brings up an Ubuntu box and starts a very simple Ansible playbook which installs the ntp deamon and makes sure that has been restarted.

# Run

To run the vagrant box and start the provisioning just type

```
vagrant up
```

Once the playbook finishes you should see something like this

```
PLAY [all] ********************************************************************

GATHERING FACTS ***************************************************************
ok: [default]

TASK: [ensure ntpd is at the latest version] **********************************
changed: [default]

NOTIFIED: [restart ntpd] ******************************************************
changed: [default]

PLAY RECAP ********************************************************************
default                    : ok=3    changed=2    unreachable=0    failed=0  
```

# Destroy

To remove the vagrant box

```
vagrant destroy -f
```
