# ctrlx-docker-mosquitto-interface

Author: samuel.gilk@boschrexroth-us.com

Description: Containerized MQTT broker for use with ctrlX CORE. Automates generation and update of MQTT topics from datalayer nodes.

Instructions:

1. Install docker and [configure buildx](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository)
2. Add user to [docker group](https://docs.docker.com/engine/install/linux-postinstall/)
3. Running docker-setup.sh will do this for you but will require a restart of the app build environment.
4. Run build_all.sh, passing target architecture as an argument (Ex. ./scripts/build_all.sh "arm64")
5. Install Container Engine app on ctrlX CORE or ctrlX CORE Virtual
6. Install built ctrlx-docker-mosquitto-interface snap on ctrlX CORE or ctrlX CORE Virtual
7. Make sure port forwarding is enabled on ctrlX CORE network adapter to access the broker externally
8. Write to ctrlx-datalayer-mqtt-interface/MQTT_Root the paths you'd like to publish to MQTT
