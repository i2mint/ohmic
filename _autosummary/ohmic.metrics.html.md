# ohmic.metrics

Example usage:

```pycon
>>> voltage = 230 # in Volts
>>> current = 10 # in Amperes
>>> power_factor_angle = cmath.acos(0.8) # in Radians
>>> voltage_harmonics = [230, 3, 5]
>>> current_harmonics = [10, 0.5, 0.8]
>>> positive_seq_voltage = 230
>>> negative_seq_voltage = 5
>>> positive_seq_current = 10
>>> negative_seq_current = 1
>>> voltage_changes = [2, 1, 3, -2, 1]
```

```pycon
>>> tp = true_power(voltage, current)
>>> ap = apparent_power(voltage, current)
>>> rp = reactive_power(voltage, current, power_factor_angle)
>>> pf = power_factor(tp, ap)
>>> v_thd = voltage_thd(voltage_harmonics)
>>> c_thd = current_thd(current_harmonics)
>>> vuf = voltage_unbalance_factor(positive_seq_voltage, negative_seq_voltage)
>>> iuf = current_unbalance_factor(positive_seq_current, negative_seq_current)
>>> pst = flicker_pst(voltage_changes)
```

```pycon
>>> print("True Power: {}W".format(tp))
True Power: 2300W
>>> print("Apparent Power: {}VA".format(ap))
Apparent Power: 2300VA
>>> print("Reactive Power: {}VAR".format(rp))
Reactive Power: (1379.9999999999998+0j)VAR
>>> print("Power Factor: {}".format(pf))
Power Factor: 1.0
>>> print("Voltage THD: {}".format(v_thd))
Voltage THD: 0.02535196476019696
>>> print("Current THD: {}".format(c_thd))
Current THD: 0.09433981132056604
>>> print("Voltage Unbalance Factor: {}%".format(vuf))
Voltage Unbalance Factor: 2.1739130434782608%
>>> print("Current Unbalance Factor: {}%".format(iuf))
Current Unbalance Factor: 10.0%
>>> print("Flicker (Pst): {}".format(pst))
Flicker (Pst): 1.378404875209022
```

### Functions

| `apparent_power`(voltage, current)            |    |
|-----------------------------------------------|----|
| `current_thd`(current_harmonics)              |    |
| `current_unbalance_factor`(...)               |    |
| `flicker_pst`(voltage_changes[, time_period]) |    |
| `power_factor`(true_power, apparent_power)    |    |
| `reactive_power`(voltage, current, ...)       |    |
| `true_power`(voltage, current)                |    |
| `voltage_thd`(voltage_harmonics)              |    |
| `voltage_unbalance_factor`(...)               |    |
