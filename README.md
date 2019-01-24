*This LICENCE is different from the LICENCE.Cypress on linux-firmware.git.*
*The files under this licence are not intended for linux-firmware.git upstreaming.*

Cypress Wifi Linux FMAC Driver Package - README
===============================================

Package Version
---------------
v4.14.52-2018\_0928


Release Date
------------
2018-09-28


Description
-----------
This is Cypress's Linux brcmfmac firmware support package.
Brcmfmac is an open-source driver project.

For more information about the Linux brcmfmac project, see:

[brcm80211 Wireless Wiki](https://wireless.wiki.kernel.org/en/users/drivers/brcm80211)


Supported Features
-----------------
* Concurrent APSTA
* P2P
* Out-of-band (OOB) interrupt
* CLM download (43455/4343w/4354/4356/43012)
* Wake on Wireless LAN
* Voice enterprise (43455)
* PMF
* WPA3-personal (43455/43012)
* VSDB (43012)
* RSDB (89342/89359)

Test Environment
----------------
* ARM (MCIMX6SX-SDB)
   * Linux v4.9.88 (NXP imx\_4.9.88\_2.0.0\_ga)
   * backports
* x86
   * Linux v4.12
   * backports


Firmware Versions
-----------------
| Chip      | FW Version    |
|-----------|---------------|
| 43455     | 7.45.173      |
| 4343W     | 7.45.98.65    |
| 4356-pcie | 7.35.180.190  |
| 4356-sdio | 7.35.349.62   |
| 4354      | 7.35.349.62   |
| 4339      | 6.37.39.92    |
| 43340     | 6.10.190.72   |
| 43362     | 5.90.247      |
| 89342     | 9.40.97       |
| 89359     | 9.40.94.1     |
| 43012     | 13.10.271.138 |


Firmware Changes
----------------
* 43455
   * --- 7.45.173 ---
   * WPA3-personal support
   * Firmware crash fix
   * Low Tx duty cycle support
   * SoftAP association fix
   * WIFI-BT coex throughput improvement
   * MFP bug fix
   * Roam time enhancement
   * --- 7.45.165 ---

* 4343W
   * --- 7.45.98.65 ---
   * Firmware crash fix
   * wowlpf feature enabled 
   * Excessive current consumption fix together operation of WLAN/BT
   * Various throughput fixes
   * --- 7.45.98.52 ---

* 4356-pcie
   * --- 7.35.180.190 ---
   * Firmware crash fix
   * MFP bug fix
   * --- 7.35.180.187 ---

* 4356-sdio
   * --- 7.35.349.62 ---

* 4354
   * --- 7.35.349.62 ---
   * Enable amsdu RX
   * RSSI computation fix
   * WIFI-BT coex throughput improvement
   * Firmware crash fix
   * --- 7.35.349.49 ---

* 4339
   * --- 6.37.39.92 ---

* 43340
   * --- 6.10.190.72 ---

* 43362
   * --- 5.90.247 ---
   * Firmware crash fix
   * --- 5.90.244 ---

* 89342
   * --- 9.40.97 ---
   * Throughput issue fix
   * AP/STA connection/ping fix
   * Fast roaming security fix
   * Firmware crash fix
   * Low Tx duty cycle support
   * RSDB extended IE fix
   * WFA 11n/11ac certification fix
   * WPS fix
   * --- 9.40.87 ---

* 89359
   * --- 9.40.94.1 ---

* 43012
   * --- 13.10.271.138 ---
   * WPA3 Personal support for 43012
   * Firmware crash fix
   * WOWLPF feature enabled
   * Qualified EXT GPIO for link loss
   * Qualified beacon loss, deauth, disassoc, net pattern with/without supplicant
   * Qualified GTKOE using both internal/external supplicant
   * Qualified ARP and DHCP lease time renewal offload
   * Added GO+STA VSDB Support
   * Added updated algorithm for beacon window
   * Added BT to WLAN wake up programming
   * Added SWDIV Enhanced by Beacon Aligned swapping
   * Updated FCREF/WLCSP nvram settings for TX board limits based on PVT results
   * Added Service DurationFix(StartFlex) request when a both\_flex request is already scheduled in the current timeslot
   * Multiple Current Optimizations
   * --- 13.10.271.107 ---


Known Issues
------------
* 4354 low throughput in 5G 40/80Mhz
* 4343w/43455 softap low throughput with iMX6UL
* 89342 rate drop in 5G 80Mhz
* 4343w/43012/43362 zero stalls while running UDP bidirectional tests
* 89342 low throughput in AP+STA, STA+AP, AP+AP RSDB modes
* 43012 single 11N WMM cert issue open
