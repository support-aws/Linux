UFW - Uncomplicated Firewall

```
sudo ufw status
```
`Status: inactive`

**List the Firewall Listening Ports:**
```
sudo ufw show listening
```
Output:
```tcp:
  22 * (sshd)
  2379 192.168.10.12 (etcd)
  2380 192.168.10.15 (etcd)
  4240 192.168.10.57 (cilium-agent)
  53 169.254.25.10 (node-cache)
  9254 169.254.25.10 (node-cache)
tcp6:
  10250 * (kubelet)
  10256 * (kube-proxy)
  10257 * (kube-controller-manager)
  10259 * (kube-scheduler)
  22 * (sshd)
  6443 * (kube-apiserver)
  9253 * (node-cache)
  9353 * (node-cache)
udp:
  53 169.254.25.10 (node-cache)
  68 192.168.10.57 (systemd-networkd)
  8472 * (-)
udp6:
  8472 * (-)
```

**Enable UFW:** Enables the firewall, activating the current rules
``` 
sudo ufw enable
```
**Disable UFW:** Disables the firewall, turning off all rules
``` 
sudo ufw disable
```
