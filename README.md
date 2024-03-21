RTT
===

SEGGER RTT Sources

https://www.segger.com/products/debug-probes/j-link/technology/about-real-time-transfer  
https://wiki.segger.com/RTT

## About this fork
Segger does not appear to regularly update their RTT github repository; probably because it gets updated on your host machine when the J-Link Software and Documentation Pack is updated. 
I prefer to use RTT as a library and explicitly add it to my projects, so I made this fork. 

## Included files

  * `RTT/`
    * `SEGGER_RTT.c`               - Main module for RTT.
    * `SEGGER_RTT.h`               - Main header for RTT.
    * `SEGGER_RTT_ASM_ARMv7M.S`    - Assembly-optimized implementation of RTT functions for ARMv7M processors.
    * `SEGGER_RTT_Printf.c`        - Simple implementation of printf (`SEGGER_RTT_Printf()`) to write formatted strings via RTT.
  * `Syscalls/`
    * `SEGGER_RTT_Syscalls_*.c`    - Low-level syscalls to retarget `printf()` to RTT with different toolchains.
  * `Config/`
    * `SEGGER_RTT_Conf.h`          - RTT configuration file.
  * `Examples/`
    * `Main_RTT_InputEchoApp.c`    - Example application which echoes input on Channel 0.
    * `Main_RTT_MenuApp.c`         - Example application to demonstrate RTT bi-directional functionality.
    * `Main_RTT_PrintfTest.c`      - Example application to test RTT's simple printf implementation.
    * `Main_RTT_SpeedTestApp.c`    - Example application to measure RTT performance. (Requires embOS)
