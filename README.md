# Avestruz Paid Relay

__Infrastructure repository for a Nostr Paid Relay__

Running a `Docker Compose` in production is not recommended and managing Kubernetes can be daunting. Fortunately there's something in the middle which is running containers under `systemd`.
[Podman](https://podman.io/) recently merged a tool called Quadlet that hides the complexity of running containers under systemd to make it easier to maintain unit files written from scratch.

Quadlet supports these unit file types:

* .container: Used to manage containers by running podman run
* .kube: Used to manage containers defined in Kubernetes YAML files by running podman kube play
* .network: Used to create Podman networks that may be referenced in .container or .kube files
* .volume: Used to create Podman volumes that may be referenced in .container files.
