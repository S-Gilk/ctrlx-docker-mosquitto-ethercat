# ctrlx-docker-mosquitto-interface

Author: S-Gilk

Description: Containerized MQTT broker for use with ctrlX CORE. Automates generation and update of MQTT topics from datalayer nodes.

Instructions:

1. Install docker (sudo snap install docker)
2. [Configure buildx](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository)
3. Add user to [docker group](https://docs.docker.com/engine/install/linux-postinstall/)
4. Running docker_setup.sh will do steps 2 & 3 for you but will require a restart of the app build environment.
5. Run build_all.sh, passing target architecture as an argument (Ex. ./scripts/build_all.sh "arm64")
6. Install Container Engine app on ctrlX CORE or ctrlX CORE Virtual
7. Install built ctrlx-docker-mosquitto-interface snap on ctrlX CORE or ctrlX CORE Virtual
8. Make sure port forwarding is enabled on ctrlX CORE network adapter to access the broker externally
9. Write to ctrlx-datalayer-mqtt-interface/MQTT_Root the paths you'd like to publish to MQTT
