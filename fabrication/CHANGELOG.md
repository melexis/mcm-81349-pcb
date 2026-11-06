# Changelog

## Version 1.0

* First version

## Version 2.0

* Add: `D14` (`SMBJ70D-M3`) TVS diode on `VBUS`
* Add: `VBUS` / `VMOTOR` current limiter & discharge circuits (`Q4`/`Q5` on `SLPWR`, `Q7`/`Q9` on `MCU`, with `FMMT306NX-TP` + `BC846BLT1G`)
* Add: Switchable `~13.5V` pre-regulator from `VMOTOR` to `U4` `VS` controlled by `MCU_12V` (`Q10` `2N7002`, `Q11` `ZXMN10A07ZTA`, `R21` `100k`, `D25` `16V` Zener, `D28` `PMEG10010ELRX`)
* Add: Overvoltage pre-regulator (`~48V` clamp) in front of `U2` (`LV2862XLVDDCR`) for up to `90V` transient `VS` protection (`Q6` `ZXMN10A07ZTA`, `R61` `100k`, `D29` `51V` Zener)
* Add: Reverse-blocking / OR-ing Schottky diodes `D16`, `D23` (`PMEG10030ELPX`) and `D28` (`PMEG10010ELRX`)
* Add: `JP1` open solder jumper to bypass `D16`, `D23`
* Update: `U4` changed to `MLX81349-KLW-BMX-000`
* Update: `U2` changed from `LMR16006YDDCR` to `LV2862XLVDDCR` with `L1 = 47uH` (`WE 74404042470`) and `R4`/`R5` (`39k`/`6k2`)
* Update: `U4` `VSM` powered from `VMOTOR` via `R57` (`33k`) and `C35` (`680nF`)
* Update: Schottky diodes `D2`, `D3`, `D8`, `D9`, `D15` upgraded from `60V` (`PMEG6010CEJF`) to `100V` (`PMEG10010ELRX`)
* Update: `MEAS_VBUS` (`R22`/`R23`) and `MEAS_VS` (`R24`/`R25`) voltage dividers changed to `95k3` (0603) / `3k` (0402) to support up to `90V`
* Update: Align passive values with EVB (`C20 = 10uF`, `C22 = 150pF`, `C23 = 100nF`, `R39 = 20mR`, `R40`/`R44`/`R50 = 0R`, `R9 = 1k`, `R10 = 2k`)
* Remove: `U8` (`BUK7Y38-100E`), `C21`, `C37`
