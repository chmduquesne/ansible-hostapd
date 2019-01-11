[![Build Status](https://travis-ci.org/chmduquesne/ansible-hostapd.svg?branch=master)](https://travis-ci.org/chmduquesne/ansible-hostapd)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-chmduquesne.hostapd-blue.svg)](https://galaxy.ansible.com/chmduquesne/hostapd)

hostapd
=======

Setup hostapd

Role Variables
--------------

`hostapd_conf` (default:[]): list of lines to put in /etc/hostapd.conf

Example Playbook
----------------

    - hosts: servers
      roles:
        - role=hostapd
      vars:
        hostapd_conf:
        - |
            interface=wlan0
            hw_mode=g
            channel=10
            ieee80211d=1
            country_code=DE
            ieee80211n=1
            wmm_enabled=1
            ssid=hello
            auth_algs=1
            wpa=2
            wpa_key_mgmt=WPA-PSK
            rsn_pairwise=CCMP
            wpa_passphrase=H3LL0

License
-------

MIT

Author Information
------------------

Christophe-Marie Duquesne
