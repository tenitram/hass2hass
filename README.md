# Description

My idea of making Home assistant available remotely with separation from local network. Idea is to run your own Home assistant instance inside your local network and maintain second instance that proxies set of components. Communication is done via mqtt, so remote instance has no direct access to local instance other than local instance listens to some mqtt topics from remote instance and publishes some topics to it. Only remote instance is accessible from internet.
Set of scripts that allow proxing Home assistant components from one instance into another via mqtt. This solution consists of the following pieces:
- mqtt bridge configuration
- Home assistant automation scripts

Components that should be proxied, have to be added to hass2hass group. Currently only sensors and switches are supported.
