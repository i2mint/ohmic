# ohmic

Tools for Electrical Power Quality Analysis.

```pycon
>>> wf = range(-10, 20)
>>> stats = power_quality_stats(wf)
>>> stats['total_power']
135
>>> float(stats['mean_power'])
4.5
```

### Functions

| [`power_quality_stats`](#ohmic.power_quality_stats)(wf)   | Compute power quality statistics from a waveform.   |
|----------------------------------------------------------------------------|-----------------------------------------------------|

### ohmic.power_quality_stats(wf)

Compute power quality statistics from a waveform.

### Modules

| [`metrics`](ohmic.metrics.html.md#module-ohmic.metrics)   | Example usage:   |
|---------------------------------------------------------------------------------|------------------|
