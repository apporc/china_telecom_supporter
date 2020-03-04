Chinese SIM Supporter
==

A Magisk module to enable support for Chinese SIM Cards(including China 
Telecom, China Unicom and China Mobile) and VoLTE for pixel 3.

This module does two things:
1. insert these lines to file
/system/vendor/rfs/msm/mpss/readonly/vendor/mbn/mcfg_sw/mbn_sw.txt 

```
    mcfg_sw/generic/China/CMCC/Commercial/Volte_OpenMkt/mcfg_sw.mbn
    mcfg_sw/generic/China/CT/Commercial/hVoLTE_OpenMkt/mcfg_sw.mbn
    mcfg_sw/generic/China/CT/Commercial/OpenMkt/mcfg_sw.mbn
    mcfg_sw/generic/China/CT/Commercial/VoLTE_OpenMkt/mcfg_sw.mbn
    mcfg_sw/generic/China/CU/Commercial/OpenMkt/mcfg_sw.mbn
    mcfg_sw/generic/China/CU/Commercial/VoLTE/mcfg_sw.mbn
```

2. add build properties

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

**NOTE**:Tested on Android 10 for China Telecom only.
