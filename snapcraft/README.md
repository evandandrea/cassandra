This is a confined snap of Apache Cassandra. To build it, run `snapcraft`
in the top-level directory.

To install and run:
```
$ sudo snap install cassandra_*.snap --force-dangerous
$ snap connect cassandra:mount-observe ubuntu-core:mount-observe
$ sudo snap connect cassandra:process-control ubuntu-core:process-control
$ sudo systemctl restart snap.cassandra.cassandra.service
```

You can check on the status of the service with:
```
systemctl status snap.cassandra.cassandra.service
```

You can set a custom cassandra.yaml with:
```
cat cassandra.yaml | sudo /snap/bin/cassandra.config-set cassandra.yaml
```

Or fetch the contents of the current cassandra.yaml with:
```
sudo /snap/bin/cassandra.config-get cassandra.yaml
```
