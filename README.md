## Homebridge Occupancy Switch

Can be used to trigger a occupancy detected event when a switch is turned on, via Siri for example.

#### Setup

`npm install -g esgie/homebridge-occupancy-switch`

And add the following to the accessories list in your Homebridge config. Change names as you wish.

```
{
  "accessory": "Occupancy Switch",
  "name": "Occupancy",
  "occupancy_sensor_name": "Occupancy Sensor",
  "switch_name": "Occupancy Switch",
  "stateful": false
}
```

Then add it to HomeKit, once added, you will need to turn on Notifications for the Occupancy sensor you just added.
If stateful flag is set to true, switch acts like a stateful switch and the corresponding occupation sensor remains triggered until the switch is manually disabled. If set to false (default), switch acts like a stateless switch and it returns back to off state immediately, hence occupation sensor is triggered in a stateless switch event manner.
