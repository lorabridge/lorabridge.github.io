# Configuration

## Environment variables

### Bridge environment variables

```yaml
# username for the mosquitto mqtt server (currently unused)
MQTT_USERNAME
# password for the mosquitto mqtt server (currently unused)
MQTT_PASSWORD
# hostname of the mosquitto mqtt server (docker container name, resolved via docker dns)
MQTT_HOST
# port under which mosquitto mqtt server is reachable
MQTT_PORT
# MQTT main topic (almost always zigbee2mqtt)
MQTT_TOPIC
# hostname of the redis server (docker container name, resolved via docker dns)
REDIS_HOST
# port under which redis server is reachable
REDIS_PORT
# redis db index to use (0 - 15)
REDIS_DB
# list name to use for pushing and pulling data
REDIS_LIST
# lorawan identifier for the bridge device (needs to be unique among bridges), consists of 16 HEX values [0-9A-F]
LORA_DEV_EUI
# key to authenticate to the gateway (needs to be same on bridge and gateway - without "\x"!) consists of 32 HEX values [0-9A-F]
LORA_DEV_KEY
# contains a credentials string used for .htpasswd files (<username>:<password hash representation>) (you can use the command below)
# valuee needs to be enclosed with quotes e.g. 'user:$2$05$mypwhash'
BASIC_AUTH
```

> Create htpasswd hashes with something like this:

```bash
htpasswd -nbB <user> <passwd>
# result should be something like admin:$2y$05$7HuXBo2Z6qj1kPSimTNsaebTkKdqfHeQtwMvvWhc7ITZQ.PKIKpda
```

### Gateway environment variables

```yaml
# mqtt topic used by chirpstack for broadcasting device info
CHIRP_TOPIC
# username for the mosquitto mqtt server (currently unused)
MQTT_USERNAME
# password for the mosquitto mqtt server (currently unused)
MQTT_PASSWORD
# hostname of the mosquitto mqtt server (docker container name, resolved via docker dns)
MQTT_HOST
# port under which mosquitto mqtt server is reachable
MQTT_PORT
# hostname of the redis server (docker container name, resolved via docker dns)
REDIS_HOST
# port under which redis server is reachable
REDIS_PORT
# redis db index to use (0 - 15)
REDIS_DB
# mqtt topic used for the device manager
DEV_MAN_TOPIC
# mqtt topic used for publishing the discovered devices
DEV_DISCOVERY_TOPIC
# mqtt topic used for publishing the device state
DEV_STATE_TOPIC
# lorawan identifier for the first (automatically created) bridge device (needs to be unique among bridges), consists of "\x" and 16 HEX values [0-9A-F] (e.g. \x0000000000000000)
CHIRPSTACK_DEV_EUI
# key to authenticate to the gateway (needs to be same on bridge and gateway) consists of "\x" and 32 HEX values [0-9A-F] (e.g. \x00000000000000000000000000000000)
CHIRPSTACK_DEV_KEY
# chripstack api secret for generating tokens
CHIRPSTACK_API_SECRET
```

> You can create the CHIRPSTACK_API_SECRET e.g. with:

```bash
openssl rand -base64 32
```