# [eBUSd](https://github.com/john30/ebusd) configuration for the Chaffoteaux Mira C Green Ultra boiler

Adapted from the great work of [ysard](https://github.com/ysard/ebusd_configuration_chaffoteaux_bridgenet) and [wrongisthenewright](https://github.com/wrongisthenewright/ebusd-configuration-ariston-bridgenet).

While these configurations are mostly functionals, some fields are different on the Mira C Green Ultra (ysard configuration is for the older, non-"Ultra" version). This is a work in progress, with the initial goal of being able to parse all messages broadcasted by the boiler.

> [!CAUTION]
> Use this configuration at your own risk. Using it with a different kind of boiler, or writing data to the wrong registers, can cause your boiler to malfunction and create a safety risk.

Example usage with an [eBUS Adapter Shield C6](https://adapter.ebusd.eu/v5-c6/index.en.html) in the default [enhanced mode](https://github.com/john30/ebusd/blob/master/docs/enhanced_proto.md):

```bash
# Replace x.x.x.x with the adapter IP address
ebusd --configpath=. --device=ens:x.x.x.x --foreground --latency=10
# received update-read boiler dhw_temperature QQ=37: 55.0
# received update-read boiler z1_fixed_temperature QQ=37: 35.0
# received update-read boiler boiler_status QQ=37: standby
# ...
```

