# FortinetConvenienceChanges
Fortinet Convenience Changes




#### stop warning me about new firmware versions, 
```bash
config system global
    set admintimeout 120
    set autorun-log-fsck enable
    set gui-date-time-source browser
    set gui-firmware-upgrade-warning disable
end
```

#### show the local in policy in the GUI, and allow unnamed policies.
```bash
config system settings
    set gui-local-in-policy enable
    set gui-allow-unnamed-policy enable
```

#### Enable auto config revisions
```bash
config system global
set revision-backup-on-logout enable
end
```

#### Fortigate CLI command alias to create shortcuts and save time
```bash
config system alias
    edit "rt"
        set command "get router info routing all"
    next
    edit "rt6"
        set command "get router info6 routing-table"
    next
    edit "gip"
        set command "get router info protocols"
    next
end
```
[Source:] https://yurisk.info/2020/02/10/fortigate-command-alias-to-save-time-on-cli/#:~:text=Aliases%20are%20available%20on%20Fortigate,at%20the%20top%20level%20only

