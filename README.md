To test this, do something like:

```bash
while true; do mosquitto_pub -h test.mosquitto.org -t 'mgdm/geo' -m '{"lat": 55.9,"lon": -4.3,"label":"hello"}'; sleep 2; done
```
