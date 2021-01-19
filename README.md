# China Telecom Supporter

A Magisk module to enable support for Chinese Telecom SIM Cards and VoLTE for Pixel 3.

1. Contents in this module:

- insert these lines to file
  /system/vendor/rfs/msm/mpss/readonly/vendor/mbn/mcfg_sw/mbn_sw.txt

```
    mcfg_sw/generic/China/CT/Commercial/hVoLTE_OpenMkt/mcfg_sw.mbn
    mcfg_sw/generic/China/CT/Commercial/OpenMkt/mcfg_sw.mbn
    mcfg_sw/generic/China/CT/Commercial/VoLTE_OpenMkt/mcfg_sw.mbn
```

- add build properties

```
    persist.dbg.ims_volte_enable=1
    persist.dbg.volte_avail_ovr=1
    persist.dbg.vt_avail_ovr=1
    persist.dbg.wfc_avail_ovr=1
    persist.radio.rat_on=combine
    persist.radio.data_ltd_sys_ind=1
    persist.radio.data_con_rprt=1
    persist.radio.calls.on.ims=1
```

2. How to use this module:

Since Magisk-Repo reject modules specific to certain devices, you need to
install this module manually. Procedure are as follows:

- Packaging and send it to your phone

```
    git clone https://github.com/apporc/china_telecom_supporter
    cd china_telecom_supporter
    zip -r /tmp/china_telecom_supporter.zip *
    adb push /tmp/china_telecom_supporter.zip /sdcard/Download/
```

- Install it from Magisk Manager UI
  Go to "Magisk Manager -> Modules -> Install from storage",
  choose china_telecom_supporter.zip and install, reboot.

**NOTE**:Tested on Android 10/11 Pixel 3
