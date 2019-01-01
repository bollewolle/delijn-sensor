# delijn-sensor

This code can be used to add a custom sensor for De Lijn public transport of Flanders (Belgium) to Home Assistant.

**_Note:_** the idea is to eventually add this to the code of Home Assistant itself

## Installation

### Step 1

Install `delijn-sensor` by copying `delijn.py` from this repo to `<config directory>/custom_components/sensor/delijn.py` of your Home Assistant instance.

**Example:**

```bash
wget https://github.com/bollewolle/delijn-sensor/raw/master/delijn.py
mv delijn.py ~/.homeassistant//custom_components/sensor/
```

### Step 2

Set up the De Lijn custom sensor.

**Example:**

```yaml
sensor:
  - platform: delijn
    sub_key: '<put your data.delijn.be subscriptionkey here>'
    nextpassage:
    - stop_id: '200552'
      max_passages: 10
    - stop_id: '201169'
      max_passages: 5
```
**_Note_**: replace with the subscription key you generated with you data.delijn.be developer account.

## Credits

Thanks to the codes of [RMV](https://www.home-assistant.io/components/sensor.rmvtransport/) and [Ruter Public Transport](https://www.home-assistant.io/components/sensor.ruter/) for all the initial work and inspiration.