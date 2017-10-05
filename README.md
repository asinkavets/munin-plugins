# NAME

nvidia_gpu_ - Wildcard plugin to monitor NVIDIA GPUs. Uses nvidia-smi utility,
usually bundled with NVIDIA GPU driver, to obtain information.

# CONFIGURATION

This is a wildcard plugin. The wildcard prefix link name should be the
value to monitor.

This plugin uses the following configuration variables:

 [nvidia\_gpu\_\*]
  env.smiexec - Location of nvidia-smi executable.
  env.warning - Warning temperature
  env.critical - Critical temperature

## DEFAULT CONFIGURATION

The default configuration is to set "env.smiexec" to /usr/bin/nvidia-smi and
assume warning and critical temperatures of 75 and 95 degrees celsius, respectively.

## EXAMPLE WILDCARD USAGE

```ln -s /usr/share/munin/plugins/nvidia_gpu_ /etc/munin/plugins/nvidia_gpu_temp```

...will monitor the temperature of available GPUs.

# TODO
- [x] Add support for GPU core clock measuring
- [x] Add support for GPU memory clock measuring
- [x] Add support for GPU utilization measuring
- [ ] Add support for number of compute processes

Use multigraphs for multiple GPUs (http://munin-monitoring.org/wiki/MultigraphSampleOutput).

# AUTHOR

Nuno Fachada <faken@fakenmc.com>

# CONTRIBUTOR(S)

2017, Aliaksandr Sinkavets <alexsinkovec@gmail.com>

# LICENSE

 GNU General Public License, version 2
 http://www.gnu.org/licenses/gpl-2.0.html

# MAGIC MARKERS

 #%# family=auto
 #%# capabilities=autoconf suggest
