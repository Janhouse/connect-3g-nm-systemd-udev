connect-3g-nm-systemd-udev
==========================

Automatically connect to 3G network once the modem becomes available on NetwrokManager (using udev and systemd).


My 3G modem (12d1:1506 Huawei Technologies Co., Ltd. E398 LTE/UMTS/GSM Modem/Networkcard) doesn't connect to the network automatically even when using NetworkManager (even with "Connect automatically" (probably because of modeswitching)), so I put together this script.

It makes udev start systemd 3g.service, that executes 3g-connect script.

3g-connect script connects to NetworkManager's LMT network.

* Put the .rules file in the udev rules folder (/etc/udev/rules.d/).
* Put the .service file in systemd system folder (/etc/systemd/system/).
* Put the 3g-connect script in /usr/bin/ folder.
