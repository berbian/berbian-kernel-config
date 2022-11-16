# berbian-kernel-config

Kernel configuration files:

- device_berbian_defconfig: Main defconfig.
- device_berbian_mer_fixes.config: Defconfig fragment with mer check tool fixes for specific device main defconfig.
- berbian_halium_waydroid.config: Fefconfig fragment with Halium and Waydroid requirements.
- berbian_extra.config: Defconfig fragment with Berbian extra configs.

The order requeired to imports fragments:
- ARCH=arch make device_berbian_defconfig device_berbian_mer_fixes.config berbian_halium_waydroid.config berbian_extra.config
