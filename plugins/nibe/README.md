# NIBE
Plugin for SmartHome https://github.com/mknx/smarthome

Requirements
============
This plugin has no requirements or dependencies.

Configuration
=============

plugin.conf
-----------
<pre>
[nibe]
    class_name = NIBE
    class_path = plugins.nibe
    serialport = /dev/ttyUSB1
</pre>

### Attributes
  * `serialport`: RS485 serial port.

items.conf
--------------
### nibe

<pre>
[heating]
    [[operating_state]]
        type = num
        nibe_reg = 31
    [[heating_curve]]
        type = num
        nibe_reg = 4
    [[circ_pump_speed_heat_p]]
        type = num
        nibe_reg = 44
    [[number_of_starts]]
        type = num
        nibe_reg = 25
    [[outdoor_temp_c]]
        type = num
        nibe_reg = 1
        sqlite = yes
    [[supply_temp_c]]
        type = num
        nibe_reg = 6
        sqlite = yes
    [[return_temp_c]]
        type = num
        nibe_reg = 7
        sqlite = yes
    [[run_time_compressor_h]]
        type = num
        nibe_reg = 24
    [[hot_water_temp_c]]
        type = num
        nibe_reg = 12
        sqlite = yes
#    [[degree_minutes]]
#        type = num
#        nibe_reg = 8
</pre>

### nibe registers
Check in plugins/__init__.py
