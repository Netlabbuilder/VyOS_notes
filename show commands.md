<details>

<summary>show version</summary>

```
vyos@vyos:~$ show version 
Version:          VyOS 1.4.0
Release train:    sagitta
Release flavor:   kvm

Built by:         Sentrium S.L.
Built on:         Tue 04 Jun 2024 10:21 UTC
Build UUID:       9bc43f00-bfd8-407f-a2b0-4ced2cc7ad5f
Build commit ID:  35dd8ae6522c78-dirty

Architecture:     x86_64
Boot via:         installed image
System type:      KVM guest

Hardware vendor:  QEMU
Hardware model:   Ubuntu 24.04 PC (i440FX + PIIX, 1996)
Hardware S/N:     
Hardware UUID:    eb5d7a11-3296-4182-94a0-cc6a153c2977

Copyright:        VyOS maintainers and contributors
vyos@vyos:~$ 

```

</details>

<details>

<summary>show configuration</summary>

```
vyos@vyos:~$ show configuration
interfaces {
    ethernet eth0 {
        hw-id 0c:5d:7a:11:00:00
    }
    ethernet eth1 {
        hw-id 0c:5d:7a:11:00:01
    }
    ethernet eth2 {
        hw-id 0c:5d:7a:11:00:02
    }
    ethernet eth3 {
        hw-id 0c:5d:7a:11:00:03
    }
    ethernet eth4 {
        hw-id 0c:5d:7a:11:00:04
    }
    ethernet eth5 {
        hw-id 0c:5d:7a:11:00:05
    }
    ethernet eth6 {
        hw-id 0c:5d:7a:11:00:06
    }
    ethernet eth7 {
        hw-id 0c:5d:7a:11:00:07
    }
    ethernet eth8 {
        hw-id 0c:5d:7a:11:00:08
    }
    ethernet eth9 {
        hw-id 0c:5d:7a:11:00:09
    }
    loopback lo {
    }
}
service {
    ntp {
        allow-client {
            address 127.0.0.0/8
            address 169.254.0.0/16
            address 10.0.0.0/8
            address 172.16.0.0/12
            address 192.168.0.0/16
            address ::1/128
            address fe80::/10
            address fc00::/7
        }
        server time1.vyos.net {
        }
        server time2.vyos.net {
        }
        server time3.vyos.net {
        }
    }
}
system {
    config-management {
        commit-revisions 100
    }
    conntrack {
        modules {
            ftp
            h323
            nfs
            pptp
            sip
            sqlnet
            tftp
        }
    }
    console {
        device ttyS0 {
            speed 115200
        }
    }
    host-name vyos
    login {
        user vyos {
            authentication {
                encrypted-password ****************
                plaintext-password ****************
            }
        }
    }
    syslog {
        global {
            facility all {
                level info
            }
            facility local7 {
                level debug
            }
        }
    }
}
vyos@vyos:~$
```

</details>

<details>

<summary>show configuration commands</summary>

```
vyos@vyos:~$ show configuration commands 
set interfaces ethernet eth0 hw-id '0c:5d:7a:11:00:00'
set interfaces ethernet eth1 hw-id '0c:5d:7a:11:00:01'
set interfaces ethernet eth2 hw-id '0c:5d:7a:11:00:02'
set interfaces ethernet eth3 hw-id '0c:5d:7a:11:00:03'
set interfaces ethernet eth4 hw-id '0c:5d:7a:11:00:04'
set interfaces ethernet eth5 hw-id '0c:5d:7a:11:00:05'
set interfaces ethernet eth6 hw-id '0c:5d:7a:11:00:06'
set interfaces ethernet eth7 hw-id '0c:5d:7a:11:00:07'
set interfaces ethernet eth8 hw-id '0c:5d:7a:11:00:08'
set interfaces ethernet eth9 hw-id '0c:5d:7a:11:00:09'
set interfaces loopback lo
set service ntp allow-client address '127.0.0.0/8'
set service ntp allow-client address '169.254.0.0/16'
set service ntp allow-client address '10.0.0.0/8'
set service ntp allow-client address '172.16.0.0/12'
set service ntp allow-client address '192.168.0.0/16'
set service ntp allow-client address '::1/128'
set service ntp allow-client address 'fe80::/10'
set service ntp allow-client address 'fc00::/7'
set service ntp server time1.vyos.net
set service ntp server time2.vyos.net
set service ntp server time3.vyos.net
set system config-management commit-revisions '100'
set system conntrack modules ftp
set system conntrack modules h323
set system conntrack modules nfs
set system conntrack modules pptp
set system conntrack modules sip
set system conntrack modules sqlnet
set system conntrack modules tftp
set system console device ttyS0 speed '115200'
set system host-name 'vyos'
set system login user vyos authentication encrypted-password '$6$QxPS.uk6mfo$9QBSo8u1FkH16gMyAVhus6fU3LOzvLR9Z9.82m3tiHFAxTtIkhaZSWssSgzt4v4dGAL8rhVQxTg0oAG9/q11h/'
set system login user vyos authentication plaintext-password ''
set system syslog global facility all level 'info'
set system syslog global facility local7 level 'debug'
vyos@vyos:~$  

```

</details>

<details>

<summary>show interfaces</summary>

```
vyos@vyos:~$ show interfaces 
Codes: S - State, L - Link, u - Up, D - Down, A - Admin Down
Interface    IP Address    MAC                VRF        MTU  S/L    Description
-----------  ------------  -----------------  -------  -----  -----  -------------
eth0         -             0c:5d:7a:11:00:00  default   1500  u/u
eth1         -             0c:5d:7a:11:00:01  default   1500  u/D
eth2         -             0c:5d:7a:11:00:02  default   1500  u/D
eth3         -             0c:5d:7a:11:00:03  default   1500  u/D
eth4         -             0c:5d:7a:11:00:04  default   1500  u/D
eth5         -             0c:5d:7a:11:00:05  default   1500  u/D
eth6         -             0c:5d:7a:11:00:06  default   1500  u/D
eth7         -             0c:5d:7a:11:00:07  default   1500  u/D
eth8         -             0c:5d:7a:11:00:08  default   1500  u/D
eth9         -             0c:5d:7a:11:00:09  default   1500  u/D
lo           127.0.0.1/8   00:00:00:00:00:00  default  65536  u/u
             ::1/128
vyos@vyos:~$
```
</details>

<details>

<summary>sudo ethtool eth0</summary>

```
vyos@vyos:~$ sudo ethtool eth0
Settings for eth0:
	Supported ports: [  ]
	Supported link modes:   Not reported
	Supported pause frame use: No
	Supports auto-negotiation: No
	Supported FEC modes: Not reported
	Advertised link modes:  Not reported
	Advertised pause frame use: No
	Advertised auto-negotiation: No
	Advertised FEC modes: Not reported
	Speed: 10000Mb/s
	Duplex: Full
	Auto-negotiation: off
	Port: Other
	PHYAD: 0
	Transceiver: internal
	Link detected: yes
vyos@vyos:~$ 
```

</details>
