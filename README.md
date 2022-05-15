This code takes a log file in csv format (passed as an extra variable) and collects/prints to a file, the max and min values for each channel parameter in the log 

Prereqs:
** Ansible and git needs to be installed on your system

Red Hat/Derivative Users:

```

yum install ansible -y

```

Windows Users:

```

https://geekflare.com/ansible-installation-windows/

```

To run the code:

```

git clone https://github.com/superky13/minMaxLogValuesHPTuners.git
cd minMaxLogValuesHPTuners
ansible-playbook displayMinAndMaxValues.yml --extra-vars "logFile=/path/to/your/log.csv"
cat or open minMaxLogValuesHPTuners/minMaxLogValues-$DATE
```
Caveat: the min values are not recorded if they are also the max values
