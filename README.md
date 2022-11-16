# berbian-kernel-config

### About branches in this repo:
- main: Contains documentation to avoid non config files in config branches to get clean clones.
- global-berbian: Contains Berbian kernel config fragments for global devices.
- specific-<device>: Contains main defconfig and other specific device config fragments.

### Config branches creation:
- main branch is a standard branch creation
- configs branches are new orphan branches created locally and pushed as new branches to github. 
  - # git switch --orphan specific-<device>

### Kernel configuration files:
- device_berbian_defconfig: Main defconfig.
- device_berbian_mer_fixes.config: Defconfig fragment with mer check tool fixes for specific device main defconfig.
- berbian_halium_waydroid.config: Fefconfig fragment with Halium and Waydroid requirements.
- berbian_extra.config: Defconfig fragment with Berbian extra configs.


### Create device specific mer fragment:
- The generated file is not a valid .config file, but a reference to create it.
   - # git clone https://github.com/mer-hybris/mer-kernel-check
   - # mer_verify_kernel_config <device>-berbian_defconfig > <device>-berbian_defconfig_check_result

### Reomended merge order:
- device_berbian_defconfig device_berbian_mer_fixes.config berbian_halium_waydroid.config berbian_extra.config
