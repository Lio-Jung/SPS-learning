# SPS-learning
learning SPS with TIA Portal

TIA Portal : TIA_Portal_STEP7_Safety_WinCC_V21.iso

PLCSIm : SIMATIC S7 PLCSIM
https://support.industry.siemens.com/cs/document/109963863/simatic-s7-plcsim-advanced-v7-0-download-incl-trial-license-?dti=0&lc=en-DE

| Adresse | Size             |
| ----      | --------------- |
| I0.0       | 1 bit           |
| IB0      | 1 byte (8bit)   |
| IW0     | 1 word (16bit)  |
| ID0     | 1 dword (32bit) |

issue : no iw, but id
solution : Driver Configuration -> dword -> word
