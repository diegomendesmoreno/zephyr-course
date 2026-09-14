# General

```bash
# Build
west build -b stm32f4_disco app -p

# Flash
west flash
```

# Kconfig

Edit prj.conf:
```Kconfig
CONFIG_BLINK_SLEEP_TIME_MS=250
```

Use menuconfig:
```bash
# press / to search, S to save, Q to quit
west build -t menuconfig
```

Command-line override:
```bash
west build -b stm32f4_disco app -p -- -DCONFIG_BLINK_SLEEP_TIME_MS=2000
```
