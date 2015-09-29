# bitmask-root
bitmask-root is an administrative service module which helps bitmask client to work on windows as well as other operating systems.

# Installation
1- Install TAP driver for windows in third-party\tap-windows directory.<br />
2- Copy .ovpn config file to third-party\openvpn.<br />
3- Add an environment variable named BITMASK_HOME and save bitmask-root directory as its value.<br />
4- Install windows service by following command (Run command prompt as administrator): <br />

```batch
windows_installer.py -install
```

5- Then start windows service:<br />

```batch
windows_installer.py -start
```

# Usage
bitmask-root has four functionalities that you can call them as a rpc client,bitmask-root supports some functionalities such as:
<br />
<ul>
<li>start_firewall</li>
<li>stop_firewall</li>
<li>start_openvpn</li>
<li>stop_openvpn</li>
</ul>

# Example
```code
client = RPCClient("tcp://%s:%s" % (127.0.0.1, 8080))
client.start_firewall()
```

