Payload format as built is:

```json
{
  "lat": 55.9,
  "lon": -4.3,
  "label": "hello" // Displayed when clicking the marker
}
```

The label is added unmodified to the marker. This is probably insecure! Make sure you trust or validate it.

To test this, do something like:

```bash
while true; do mosquitto_pub -h test.mosquitto.org -t 'mgdm/geo' -m '{"lat": 55.9,"lon": -4.3,"label":"hello"}'; sleep 2; done
```
