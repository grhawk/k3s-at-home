Usage
----
 
 ### Install needed ansible modules:
 - `ansible-galaxy collection install community.kubernetes`
 
``` bash
ansible-playbook -v site.yml  -i inventory/hosts.ini -e "{\"op_credentials\": \"$(op item  --vault k3s@home get c2fiwogrm2ohhy7jijml4fvjem --fields label=base64)\", \"op_token\": \"$(op item --vault k3s@home get eib45kbot2lyxxugsu7ikrsazq --fields label=base64)\", \"my_mail\": \"$(op item get fxwpqrzpncksdezymgzp6i7fbm --fields label=email)\", \"prometheus_webhook\": \"$(op  --vault k3s@home item get owdhh7g2bq4oyyjknal4bwoln4 --fields label=prometheus-webhook)\", \"prometheus_heartbeat\": \"$(op  --vault k3s@home item get owdhh7g2bq4oyyjknal4bwoln4 --fields label=prometheus-heartbeat)\", \"mqtt_username\": \"$(op item get 3gjbzmqksledyacuo2h253w7tu --fields label=mosquitto-username)\", \"mqtt_password\": \"$(op item get 3gjbzmqksledyacuo2h253w7tu --fields label=mosquitto-password)\", \"zigbee_coordinator\": \"$(op item get 3gjbzmqksledyacuo2h253w7tu --fields label=zigbee-coordinator)\", \"zigbee2mqtt\": {\"network_key\": \"$(op item get 3gjbzmqksledyacuo2h253w7tu --fields label=network-key)\"}}"
```

