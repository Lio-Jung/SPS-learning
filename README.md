# SPS-learning
learning SPS with TIA Portal

-----------------------------------------


Was 

Simulationsprojekt zur industriellen Automatisierung: eine Paketsortieranlage in Factory I/O, gesteuert über TIA Portal und S7-PLCSIM Advanced. Pakete werden nach Größe erkannt und auf verschiedene Förderstrecken bzw. Ausgänge sortiert.


Wie

Anlage in Factory I/O modelliert (Förderer, Sensorik, Weichen)
SPS-Programm in FBD (Funktionsplan) in TIA Portal V21 erstellt
S7-PLCSIM Advanced als virtuelle SPS; Verbindung zu Factory I/O über Ethernet/WLAN
Ein- und Ausgänge in TIA Portal angelegt und mit Factory I/O verknüpft
Problem gelöst: Factory I/O liefert Paketgröße als DWord (ID) statt Word (IW) → Anpassung in der Driver Configuration (DWord → Word)


Womit
TIA Portal V21 · SIMATIC S7-PLCSIM Advanced V7.0 · Factory I/O


Was ich gelernt habe

Aufbau und Inbetriebnahme einer SPS-Simulation (CPU, I/O, Download, Schutz-Einstellungen)
Signalfluss: Sensor → SPS-Logik → Aktoren (Förderer, Weiche)
Adressierung (Bit/Byte/Word/DWord) und Schnittstelle zwischen Simulation und SPS
Fehlersuche bei Verbindungs- und Download-Problemen (PLCSIM, CPU-Auswahl, Netzwerk)
Dokumentation des Lernprozesses (Screenshots, Videos)


Hinweis
Reine Simulation; keine reale Schaltschrank-Verdrahtung. Zeigt aber Eigeninitiative und Vorbereitung auf Steuerungs- und Automatisierungstechnik im Rahmen einer EBT-Ausbildung.
--------------------------------


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
