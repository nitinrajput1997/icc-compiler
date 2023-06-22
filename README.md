# icc-compiler

### Use command line to download installation script
```
wget https://registrationcenter-download.intel.com/akdlm/irc_nas/18211/l_HPCKit_p_2021.4.0.3347.sh
```

### Execute downloaded script via
```
sudo sh <script-name>.sh -a --silent --eula accept
```
### Configure Environment Variable
```
 vi ~/.bashrc
```

**Append following environment variable**
```
export INTEL_ONEAPI_ROOT=/opt/intel/oneapi
export PATH=$PATH:$INTEL_ONEAPI_ROOT/compiler/2021.4.0/env:$INTEL_ONEAPI_ROOT/compiler/2021.4.0/linux/bin/intel64
```
**Execute**
```
source .bashrc --force
```
### Create iccvar.sh

Because we need iccvars.sh in other section and the file in current version is called vars.sh, we copy vars.sh to iccvars.sh.

```
sudo cp /opt/intel/oneapi/compiler/2021.4.0/env/vars.sh /opt/intel/oneapi/compiler/2021.4.0/env/iccvars.sh
```
### Verify installation
Check icc
```
icc --version
```
