### Use `nmcli` from a Debian container without installing NetworkManager

This repo demonstrates how to download, extract and run the `nmcli` utility from the `network-manager` Debian package without the need for installing the full NetworkManager suite.

Internally `nmcli` communicates through D-Bus with the NetworkManager service running on the host OS. That is to say `nmcli` can be run inside a resin container without any need for running NetworkManager service next to it. Moreover installing NetworkManager inside the application container is dangerous if the NetworkManager service is not masked. Downloading and extracting `nmcli` is a safer approach that additionally saves bytes.

For more details please check the [Dockerfile template](./Dockerfile.template) of this project.
