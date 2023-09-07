# Changelog

## **0.5.9** 2023.09.07 *EDGE*

- Improve error handling on initial read
- mysensors error handling
- Improve logging

## **2023.08.27-0.5.7**

- Bugfix: read_batch_size
- 5ms delay before reads
- Average for numeric types
- Better warnings & exceptions
  - Warn if no value read
  - re-run on any exception
  - list exception per group of sensors (or batch)
- New defaults

  ```yaml
  READ_ALLOW_GAP: 2
  READ_SENSORS_BATCH_SIZE: 20
  ```

## **2023.08.23-0.5.5**

- Group error logs
- Scheduler updates & test

## **2023.08.22-0.5.4**

- Minor change to schedules (might address #172 + test coverage)
- Better logging of Schedules & selected sensors
- Update to documentation & links

## **2023.08.17-0.5.3**

Minor fixes

## **2023.08.17-0.5.2**

**Read the PR text & docs BEFORE you upgrade!**

Please read the description here: <https://github.com/kellerza/sunsynk/pull/168>

Especially if you use sensor modifiers. See <https://kellerza.github.io/sunsynk/reference/schedules>

## **2023.08.06-0.4.0**

- Added the pysolarman driver

## **2023.07.19-0.3.7**

- sunsynk 0.3.7
  - bugfix writing numeric sensors

- Multi & Dev Addon
  - Update to pyyaml 6.0.1

## **2023.05.19-0.3.6**

- sunsynk 0.3.6
  - priority_mode -> priority_load (as a switch)

- Multi Addon
  - Fixed switches & binary_sensors (selects will change to HASS switches)

## **2023.05.18-0.3.5**

- sunsynk 0.3.5
  - Reworked 1ph essentials sensor - refer to definitions.py

    Essential power
    - <https://powerforum.co.za/topic/8646-my-sunsynk-8kw-data-collection-setup/?do=findComment&comment=147591>

    Essential 1 power
    - dev & normal version, see <https://github.com/kellerza/sunsynk/issues/134>

    Essential 2 power
    - early-2023 see <https://github.com/kellerza/sunsynk/issues/75>

  - Additional sensors to support all the options in @slipx's power flow card
    - Inverter Current
    - Generator Input (235) - this might explain the difference on the essentials sensor value...
    - Use Timer - see <https://github.com/kellerza/sunsynk/discussions/137>

## **2023.05.05-0.3.4**

- sunsynk 0.3.4
  - Improve test coverage

- Multi-Addon
  - multiple inverters beta release (`SENSORS_FIRST_INVERTER` not yet supported)
  - Improve test coverage

## **2023.04.22-0.3.3**

- sunsynk 0.3.3
  - Update pysunsynk driver
  - Added date sensor (MQTT text entity)
  - Improve test coverage
  - Changed switch entity

- Multi-Addon

## **2023.04.20-0.3.2**

- If you have a Serial, either try pymodbus serial or use mbusd

- update pymodbus to 3.2.2
  - Tcp seems to work (only been running for a short while)
  - Serial not tested

- umodbus
  - TCP is stable
  - Serial is currently not working

- paho-mqtt 1.6.1

- **2023.04.20b-0.3.2**  - bugfix log

## **2023.04.17-0.3.1**

- split out mqtt_entity

## **2023.03.19b-0.3.1**

- Fixed MQTT reconnect logic #94

## **2023.03.19-0.3.1**

- Initial release of the multi addon
- It only supports a single inverter today
- Select between single-phase & three-phase sensor definitions
- Supports custom sensors in /share/hass-addon-sunsynk/mysensors.py