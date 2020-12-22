# PBRP device tree for Galaxy S5 (International Qualcomm, Americas, and Oceanic)

[![Build Status](https://travis-ci.com/JuanLiz/android_device_samsung_klte-pbrp.svg?branch=android-7.1)](https://travis-ci.com/JuanLiz/android_device_samsung_klte-pbrp)

## How To Build

```bash
# Initialize the latest stable branch
repo init -u git://github.com/PitchBlackRecoveryProject/manifest_pb.git -b android-7.1

# Sync the latest stable branch
repo sync
```

Add to `.repo/local_manifests/klte.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
 <project path="device/samsung/klte" name="JuanLiz/android_device_samsung_klte-pbrp" remote="github" revision="android-7.1" />
</manifest>
```

Then run `repo sync` again to check it out.

⚙️ Build

```bash
cd <source-dir>
. build/envsetup.sh
lunch omni_klte-eng
mka recoveryimage
````

Kernel sources are available at: <https://github.com/jcadduono/nethunter_kernel_klte/tree/twrp-6.0>

Credits to <a href="https://github.com/jcadduono" target = "_blank">@jcadduono</a> for the tree used as a base.

Credits to <a href="https://github.com/IcemanDev" target = "_blank">@IcemanDEV</a> for his fix for aroma installer.

Credits to <a href="https://github.com/Yilliee" target = "_blank">@Yilliee</a> , <a href="https://github.com/DarthJabba9" target = "_blank">@DarthJabba9</a> for various other edits
