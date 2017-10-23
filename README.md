# HOW-TO Build
* Initialize the repository
   
   ```sh
   repo init -u git://github.com/LineageOS/android.git -b cm-10.1
* Add my manifest to the .repo/local_manifests folder
   
   
   ```sh
   cp local_manifest.xml .repo/local_manifests
* Sync latest LineageOS 10.1 sources
  
  
  ```sh
   repo sync -j20 --force-sync
* Apply all Patches
   
   
   ```sh
   cp device/dell/gallo/patch/device/common/gps/* device/common/gps
   cp device/dell/gallo/patch/hardware/libhardware_legacy/vibrator/vibrator_gallo.c hardware/libhardware_legacy/vibrator/vibrator_gallo.c
   cp -rf device/dell/gallo/patch/vendor/cm/proprietary vendor/cm/proprietary
   patch -p1 < device/dell/gallo/patch/PATCH

